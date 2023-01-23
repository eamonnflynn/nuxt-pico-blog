<template>
    <div>
      <h1>Blog</h1>
      
        <article v-for="post in posts" :key="post.id">
        <div class="grid">
          <div>
            <nuxt-link :to="`${post._path}`">
             <nuxt-img :src="`${post.image}`" height="250px" />
            </nuxt-link>
          </div>
          <div>
            <h2>{{ post.title }}</h2>
          <p>{{ post.description }}</p>
          <p>{{ formatDate(post.pubDate) }}</p>
          <nuxt-link :to="`${post._path}`">Read more</nuxt-link>
          </div>
        </div>
          
        </article>
     
     
    </div>
  </template>

<script setup >
import dayjs from 'dayjs';
const posts = await queryContent('blog')
.sort({ pubDate: -1 })
      .find();


      function  formatDate(dateString) {
            const date = dayjs(dateString);
                // Then specify how you want your dates to be formatted
            return date.format('dddd MMMM D, YYYY');
        }

</script>

<style scoped>

</style>


