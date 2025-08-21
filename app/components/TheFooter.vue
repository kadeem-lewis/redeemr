<script setup lang="ts">
const year = ref(new Date().getFullYear());
</script>
<template>
  <footer class="pb-4">
    <p class="text-center">&copy; {{ year }} Redeemr.net</p>
  </footer>
</template>
