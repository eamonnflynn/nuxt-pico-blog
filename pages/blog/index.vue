<template>
    <div>
      <h1>Blog</h1>
      <ul>
        <li v-for="post in posts" :key="post.id">
          <nuxt-link :to="`${post._path}`">{{ post.title }}</nuxt-link>
        </li>
      </ul>
     
    </div>
  </template>

<script setup >
const posts = await queryContent('blog')
.sort({ pubDate: -1 })
      .find()

</script>

<style scoped>

</style>


