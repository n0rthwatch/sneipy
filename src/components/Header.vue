<template>
  <header class="header">
    <StdButton @click="tg.close()" :text="Закрыть"></StdButton>
    <span class="username">
      {{ username }}
    </span>
  </header>
</template>


<script setup>
import StdButton from './StdButton.vue';

const tg = window.Telegram.WebApp;
const username = tg.initDataUnsafe.user.username;
</script>


<style>

</style>