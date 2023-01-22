<template>
  <NuxtLayout>
    <NuxtLoadingIndicator :height="10" :duration="3000" :throttle="400" />
    <NuxtPage />
  </NuxtLayout>
</template>

<script lang="ts" setup>
import { AppConfigInput } from "@nuxt/schema";

const app = useAppConfig() as AppConfigInput;
useHead({
  title: app.name,
  titleTemplate: `%s - ${app.name}`,
  meta: [
    { name: "viewport", content: "width=device-width, initial-scale=1" },
    {
      hid: "description",
      name: "description",
      content: app.name,
    },
  ],
  link: [{ rel: "icon", type: "image/x-icon", href: "/favicon.ico" }],
});
</script>
