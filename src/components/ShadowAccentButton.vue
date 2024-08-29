<template>
  <div :class="props.class" class="shadow_btn" @click="props.action" :id="props.id">
    <p class="btn_title">{{ props.title }}</p>
    <p class="btn_text">{{ props.text }}</p>
    <div class="btn_timer">
      <div class="timer_line" :style="{ width: `${props.timer}%` }">
        {{ props.timer }}
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  id: Number,
  text: String,
  class: String,
  action: Function,
  title: String,
  timer: Number,
})

// if (timer <= 0) {
//   props.class.add('5')
// } 
</script>
<style>
.shadow_btn {
  /* display: inline-block; */
  position: relative;
  background: var(--tg-theme-background-color);
  color: var(--tg-theme-text-color);
  padding: 10px 20px;
  border: none;
  text-wrap: nowrap;
  box-shadow: 0 0 4px 3px rgba(0, 0, 0, 0.2);
  border-radius: 7px;
  text-align: center;
  cursor: pointer;
}

.btn_title {
  font-weight: 800;
  font-size: 14px;
}

.btn_text {
  font-weight: 800;
  font-size: 18px;
  margin-bottom: 10px;
}

.full_width {
  width: 100%;
}

.btn_timer {
  width: 100%;
  position: absolute;
  height: 15px;
  bottom: 0;
  left: 0;
  background: #0000005d;
  border-radius: 0 0 7px 7px;
}

.timer_line {
  background: var(--rainbow-gradient);
  height: 100%;
  border-radius: 0 0 7px 7px;
  opacity: .5;
}
</style>