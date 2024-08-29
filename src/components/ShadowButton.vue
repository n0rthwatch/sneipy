<template>
  <div :class="props.class" class="shadow_btn" @click="props.action" :id="props.id">
    <p class="btn_title">{{ props.title }}</p>
    <p class="btn_text">{{ props.text }}</p>
  </div>
</template>
<script setup>
const props = defineProps({
  id: Number,
  text: String,
  class: String,
  action: Function,
  title: String,
})
</script>
<style>
.shadow_btn {
  /* display: inline-block; */
  background: var(--tg-theme-background-color);
  color: var(--tg-theme-text-color);
  padding: 5px 12px;
  border: none;
  text-wrap: nowrap;
  box-shadow: 0 0 4px 3px rgba(0, 0, 0, 0.2);
  border-radius: 7px;
  text-align: center;
  cursor: pointer;
}

.btn_title {
  font-weight: 600;
  letter-spacing: 1px;
  font-size: 10px;
}

.btn_text {
  font-weight: 800;
  font-size: 16px;
}

.full_width {
  width: 100%;
}
</style>