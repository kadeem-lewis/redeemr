<script setup lang="ts">
import { EXTERNAL_LINKS } from "~/constants/links";

const items = ref([
  {
    label: "youtube",
    subtitle: "My main Youtube channel",
    link: EXTERNAL_LINKS.youtubeUrl,
  },
  {
    label: "framedle",
    subtitle: "My wordle-like Warframe guessing game",
    link: EXTERNAL_LINKS.framedleUrl,
  },
  {
    label: "discord",
    subtitle: "Join my discord server",
    link: EXTERNAL_LINKS.discordInviteLink,
  },
  {
    label: "bluesky",
    subtitle: "Follow me on Bluesky",
    link: EXTERNAL_LINKS.blueskyUrl,
  },
  {
    label: "youtube archives",
    subtitle: "Archive of quests and livestreams",
    link: EXTERNAL_LINKS.youtubeArchiveUrl,
  },
]);
</script>
<template>
  <div class="flex flex-col gap-8">
    <div class="text-center text-xl">
      <p>
        Hello world, I'm Redeemr. I'm a software developer ( as you can tell )
        who makes Warframe content.
      </p>
      <p>Learn more about me by checking out one of the links below.</p>
    </div>
    <div class="flex justify-center">
      <div class="flex flex-col gap-8 max-w-80 justify-center">
        <UButton
          v-for="item in items"
          :key="item.label"
          :to="item.link"
          variant="outline"
          size="xl"
          :ui="{ base: 'rounded-none' }"
        >
          <div class="flex flex-col gap-2 items-center w-full">
            <span class="capitalize text-lg">{{ item.label }}</span>
            <span class="text-center">{{ item.subtitle }}</span>
          </div>
        </UButton>
      </div>
    </div>
    <p class="text-center text-xl">
      For inquiries, please contact me at
      <ULink href="mailto:contact@redeemr.net">contact@redeemr.net</ULink>.
    </p>
  </div>
</template>
