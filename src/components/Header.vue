<template>
    <header>
        <h1>{{title}}</h1>
    </header>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: "Header",
  props: {
      title: {
          type: String,
          default: "Epic Website"
      }
  }
});
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 1em;
        background-color: aqua;
    }
</style>