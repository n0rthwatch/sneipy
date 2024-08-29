<template>
  <section>
    <div class="cat__clicker" @click="handleClick">
      <img :class="{
        'cat__clicker_img': true,
        clicked: isClicked
      }" src="../assets/black-cat.png" alt="">
    </div>
    <div class="cat__buttons">
      <ShadowAccentButton timer="70" text="1312323" title="1231313"></ShadowAccentButton>
      <ShadowAccentButton timer="0" text="1312323" title="1231313"></ShadowAccentButton>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import ShadowAccentButton from '../components/ShadowAccentButton.vue';

const isClicked = ref(false);

const handleClick = () => {
  isClicked.value = true;
  setTimeout(() => {
    isClicked.value = false;
  }, 50);  
};
</script>

<style scoped>
section {
  position: relative;
  padding: 20px 0 50px;
  z-index: 10;
  height: 100%;
  width: 100%;
  background: var(--tg-theme-secondary-bg-color);
  border-radius: 20px;
  box-shadow: 0 0 4px 3px rgba(0, 0, 0, 0.2);

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  justify-content: space-between;
}

.cat__clicker {
  /* max-height: 300px; */
}

.cat__clicker_img {
  width: 100%;
  height: 100%;
  filter: drop-shadow(0px 5px 10px #000);
  transition: transform 0.05s ease;
}

.cat__clicker_img.clicked {
  transform: scale(0.96);
}

.cat__buttons {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
}
</style>