<script lang="ts" setup>
import { AppConfigInput } from "@nuxt/schema";
const app = useAppConfig() as AppConfigInput;
</script>

<template>
  <header>
    <h2>
      {{ app.name }}
    </h2>
    <nav>
      <ul>
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/blog">Blog</NuxtLink></li>
        <li><NuxtLink to="/about">About</NuxtLink></li>
      </ul>
    </nav>
  </header>
  <hr/>
</template>
