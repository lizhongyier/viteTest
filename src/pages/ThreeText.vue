<template>
  <div class="demo"></div>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
import ThreeJs from '@/three/index';
export default defineComponent({
  name: 'ThreeText',
  setup: () => {
    new ThreeJs();
  },
});
</script>
<style lang="less" scoped></style>
