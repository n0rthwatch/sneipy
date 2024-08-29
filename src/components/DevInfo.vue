<template>
  <div>
    <pre class="dev">{{ info }}</pre>
  </div>
</template>

<script setup>
import { inject, ref } from 'vue';
const tg = inject('tg')

const info = ref({
  initData: tg.initData,
  initDataUnsafe: tg.initDataUnsafe,
  version: tg.version,
  colorScheme: tg.colorScheme,
  themeParams: tg.themeParams,
  isExpanded: tg.isExpanded,
  viewportHeight: tg.viewportHeight,
  viewportStableHeight: tg.viewportStableHeight,
  headerColor: tg.headerColor,
  backgroundColor: tg.backgroundColor,
  isClosingConfirmationEnabled: tg.isClosingConfirmationEnabled,
  platform: tg.platform,
  isIframe: tg.isIframe,
})

console.log(info.value)

</script>

<style scoped>
</style>