<template>
  <div>
    <h1 v-for="article in data">{{ article.title }}</h1>
  </div>
</template>
<script lang="ts" setup>
import { ref, computed } from 'vue'
const articles = ref([])

const { data, pending, error, refresh } = await useAsyncData(  'articles',  () => $fetch('https://notion-api.splitbee.io/v1/table/What-is-Nuxt-Getting-started-with-create-nuxt-app-309e15c224034b099ee041e5b82e1e47'))
</script>
