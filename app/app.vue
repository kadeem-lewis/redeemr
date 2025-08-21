<script setup lang="ts">
useSeoMeta({
  title: "Redeemr",
  description: "Home of all things Redeemr",
});
</script>
<template>
  <UApp>
    <NuxtRouteAnnouncer />
    <UContainer class="flex flex-col gap-4 min-h-dvh">
      <TheHeader />
      <main class="h-full flex items-center justify-center grow">
        <NuxtPage />
      </main>
      <TheFooter />
    </UContainer>
  </UApp>
</template>
