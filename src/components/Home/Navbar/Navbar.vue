<script setup lang="ts">
import { toggleDark } from '~/composables'

const { t } = useI18n()

</script>

<template>
  <nav text-xl mt-6>
    <router-link class="icon-btn mx-2" to="/" :title="t('button.home')">
      <div i-carbon-campsite />
    </router-link>

    <button class="icon-btn mx-2 !outline-none" :title="t('button.toggle_dark')" @click="toggleDark()">
      <div i="carbon-sun dark:carbon-moon" />
    </button>

    <router-link class="icon-btn mx-2" to="/about" :title="t('button.about')">
      <div i-carbon-dicom-overlay />
    </router-link>
  </nav>
</template>
