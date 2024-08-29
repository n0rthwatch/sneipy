<template>
  <div class="wrapper">
    <Header></Header>
    <RouterView />
    <MainMenu></MainMenu>
  </div>
  <DevInfo/>
</template>

<script setup>
import { provide } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue';
import MainMenu from './components/MainMenu.vue';

import DevInfo from './components/DevInfo.vue';

const tg = window.Telegram.WebApp;

provide('tg', tg)
</script>


<style>
.wrapper {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items:normal;
  justify-content: flex-start;
}
</style>
