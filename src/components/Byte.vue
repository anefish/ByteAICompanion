<script setup lang="ts">
// import { ref } from "vue";

import { onMounted } from "vue";

defineProps<{ msg: string }>();

onMounted(() => {
  setTimeout(() => {
    window.location.href =
      "https://x.com/i/grok?text=" +
      encodeURIComponent("Woof, let me talk to Byte.");
  }, 3000);
});
</script>

<template>
  <div class="fullscreen container">
    <!-- <img class="" src="../assets/byte1.jpg" alt="" /> -->
  </div>
</template>

<style scoped>
.container {
  background-image: url("../assets/byte1.jpg");
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover; /* 关键：撑满容器，等比裁剪，不变形 */
  /* background-attachment: fixed; 可选：固定背景，滚动时不动（视差效果） */
}
</style>
