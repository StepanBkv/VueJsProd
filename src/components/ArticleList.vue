<template>
  <div class="hello">
      <h1>{{ msg }} </h1>
      <ul v-if="articles.length">
        <Article
         v-for="article in articles"
         :key="article.id"
         :title="article.title"
         :body="article.body"
        />
    </ul>
    <p v-else>  
      No article in the list.
    </p>
    </div>
</template>
<script>
import Article from './Article.vue'

export default {
  name: 'ArticleList',
  props: {
    msg: String
  },
  components:{
    Article
  },
  data(){
    return {
      articles:[
        {
          id: 1,
          title: 'Title 1',
          body: 'Learn Vue'
        },
        {
          id: 2,
          title: 'Title 2',
          body: 'Learn about single-file components'
        },
        {
          id: 3,
          title: 'Title 3',
          body: 'Fail in love'
        }
      ]
    }
  },
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;

}
a {
  color: #42b983
}
</style>