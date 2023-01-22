
<script lang="ts" setup>
import { AppConfigInput } from '@nuxt/schema'
const app = useAppConfig() as AppConfigInput
</script>

<template>
      <footer >
      <div class="">
        <div class="mb-1">
          {{ app.name }}
        </div>
        <div class="">
          Copyright © 2022 <a :href="app.author.link">{{ app.author.name }}</a
          >. All rights reserved. Made with <span>❤</span>
          <div class="">
            <span class="">
              design by <a :href="app.author.link">{{ app.author.name }}</a>
            </span>
           
          </div>
        </div>
      </div>
  </footer>
</template>

