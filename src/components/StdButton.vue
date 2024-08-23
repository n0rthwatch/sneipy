<template>
  <button :class="props.class" class="std-btn">{{  }}</button>
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
  background: var(--tg-theme-section-bg-color);
  color: var(--tg-theme-text-color);
  padding: 10px 15px;
  font-size: 14px;
}
</style>