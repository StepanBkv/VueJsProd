<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <ArticleList msg="Article"/>
  </div>
</template>

<script>
// @ is an alias to /src
import ArticleList from '@/components/ArticleList.vue'

export default {
  name: 'Home',
  components: {
    ArticleList
  }
}
</script>
