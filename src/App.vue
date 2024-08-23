<script setup>
import { RouterLink, RouterView } from 'vue-router'
const tg = window.Telegram.WebApp;


</script>

<template>
  <RouterView />
  <button @click="tg.close()">Закрыть</button>
</template>

<style scoped>

</style>
