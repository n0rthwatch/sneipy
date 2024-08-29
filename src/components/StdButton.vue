<template>
  <button :class="props.class" class="std-btn" :id="props.id">{{ props.text }}</button>
</template>
<script setup>
const props = defineProps({
  id: Number,
  text: String,
  class: String,

})
</script>
<style>
.std-btn {
  background: var(--tg-theme-button-color);
  color: var(--tg-theme-text-color);
  padding: 10px 20px;
  font-size: 14px;
  border: none;
  text-wrap: nowrap;
}
</style>