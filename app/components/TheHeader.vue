<script setup lang="ts">
import type { NavigationMenuItem } from "@nuxt/ui";
import { EXTERNAL_LINKS } from "~/constants/links";

const items = ref<NavigationMenuItem[]>([
  {
    label: "contact",
    to: "/contact",
  },
  {
    label: "framedle",
    to: "/framedle",
  },
]);

const iconLinks = ref<NavigationMenuItem[]>([
  {
    icon: "my-icon-youtube",
    to: EXTERNAL_LINKS.youtubeUrl,
    external: true,
  },
  {
    icon: "my-icon-discord",
    to: EXTERNAL_LINKS.discordInviteLink,
    external: true,
  },
  {
    icon: "my-icon-bluesky",
    to: EXTERNAL_LINKS.blueskyUrl,
    external: true,
  },
]);
</script>
<template>
  <header class="flex items-center justify-between py-2">
    <div>
      <ULink to="/" class="flex gap-1 items-center">
        <NuxtImg src="/logo.png" height="40" width="40" alt="Redeemr logo" />
        <span>Redeemr</span>
      </ULink>
    </div>
    <UNavigationMenu :items="items" class="capitalize text-base" highlight />
    <UNavigationMenu :items="iconLinks" collapsed />
  </header>
</template>
