<script setup lang="ts">
import { EXTERNAL_LINKS } from "~/constants/links";
</script>
<template>
  <div class="flex flex-col items-center justify-center gap-4">
    <h1 class="text-4xl font-bold">
      Discover high quality guides to elevate your Warframe experience.
    </h1>
    <p>
      Learn about the most obscure mechanics all the way to the most popular
      content.
    </p>
    <UButton :to="`${EXTERNAL_LINKS.youtubeUrl}/videos`"
      >Check out my Youtube Videos</UButton
    >
  </div>
</template>
