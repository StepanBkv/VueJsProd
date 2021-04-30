<template>
    <div>
        <h3>{{ title }} </h3>
        <div>
            {{ body }}
        </div>
    </div>
</template>

<script>
export default {
    name: 'Article',
    props: {
        title: String,
        body: String
    }
}
</script>

<style scoped>
h3{
    color: #999
}
</style>