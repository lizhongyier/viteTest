<template>
  <div>
    {{ name }}
    {{ count }}
    <button @click="changCount">+</button>
  </div>
</template>
<script lang="ts">
import { defineComponent, onMounted } from 'vue';
import { useUserStore } from '@/store/user';
import { storeToRefs } from 'pinia';
export default defineComponent({
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Login',
  // eslint-disable-next-line @typescript-eslint/no-empty-function
  setup: () => {
    const { name, count } = storeToRefs(useUserStore());
    console.log(name);
    const changCount = () => {
      useUserStore().increment();
    };
    onMounted(() => {
      console.log('wahahah');
    });
    return {
      changCount,
      name,
      count,
    };
  },
});
</script>
<style lang="less" scoped></style>
