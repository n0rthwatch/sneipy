<template>
  <header class="header">
    <div class="header__wrapper">
      <div class="header__top">
        <span class="username">{{ username }}</span>
        <ArrowLink text="Telegram?" link="https://t.me/vivus151" />
      </div>
      <div class="header__buttons">
        <ShadowButton text="392" :action="btnPressHandler" title="Level" />
        <ShadowButton text="+ 3’313’461" :action="btnPressHandler" title="Per hour" class="full_width" />
        <ShadowButton text="192’837’465" :action="btnPressHandler" title="Balance" class="full_width" />
      </div>
    </div>
    <div class="header__exp_wrapper">
      <div class="exp__line"></div>
    </div>
    <!-- <StdButton @click="tg.close()" text="В пизду это всё..."></StdButton> -->
  </header>
</template>


<script setup>
import { inject } from 'vue';
import StdButton from './StdButton.vue';
import ArrowLink from './ArrowLink.vue';
import ShadowButton from './ShadowButton.vue';

const tg = inject('tg')
const username = tg?.initDataUnsafe?.user?.username || 'Guest';

function btnPressHandler() {
  alert('Тут что-то будет');
}
</script>


<style>
.header__wrapper {
  margin: 8px 12px;
}

.username {
  text-transform: uppercase;
  font-weight: 900;
  font-size: 18px;
}

.header__top {
  margin-bottom: 15px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.header__buttons {
  margin-bottom: -30px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  gap: 15px;
}

.header__exp_wrapper {
  position: relative;
  z-index: 1;
  width: 100%;
  height: 50px;
  background: rgba(0, 0, 0, .4);
  border-radius: 20px 20px 0 0;
  transform: translateY(40px);
}

.exp__line {
  position: relative;
  z-index: 1;
  width: 80%;
  height: 100%;
  background: var(--rainbow-gradient);
  opacity: .6;
  border-radius: 20px 20px 0 0;
}
</style>