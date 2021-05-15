<template>
  <button @click="onClick()">{{ title }}</button>
</template>

<script>
export default {
  props: {
    title: String,
  },
  methods: {
    onClick() {
      this.$emit("onclick");
    },
  },
};
</script>

<style>
</style>