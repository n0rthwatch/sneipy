<template>
  <a class="arrow_link" :class="props.class" :href="props.link">{{ props.text }} ></a>
</template>


<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  class: String,
  link: { type: String, required: true },
  text: { type: String, required: true },
})
</script>


<style>
.arrow_link {
  text-decoration: none;
  font-weight: 400;
  font-size: 14px;
  color: var(--tg-theme-text-color)
}
</style>