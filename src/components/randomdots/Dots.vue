<template>
  <Dot :key="dot.id" v-for="dot in this.dots" :data="dot" />
</template>

<script>
import Dot from "./Dot.vue";
export default {
  components: { Dot },
  props: {
    dots: Array,
  },
};
</script>

<style scope>
</style>