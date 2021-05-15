<template>
  <AnotherButton title="Add Dot" @onclick="onclick" />
  <div class="RandomDots">
    <Dots :dots="dots" />
  </div>
</template>

<script>
import AnotherButton from "./AnotherButton.vue";
import Dots from "./Dots.vue";
export default {
  name: "RandomDotts",
  components: {
    AnotherButton,
    Dots,
  },
  data() {
    return {
      dots: [],
    };
  },
  created() {
    this.dots = []; //runs when creaeted resets the dots.
  },
  methods: {
    onclick() {
      const dot = {
        top: Math.random() * 100,
        left: Math.random() * 100,
        color: "#000",
        size: Math.random() * 10,
      };
      this.dots.push(dot);
    },
  },
};
</script>

<style scoped>
.RandomDots {
  background-color: #aa1322;
  width: 50vh;
  height: 50vh;
  position: relative;
  margin: auto;
  border: 20px solid #aa1322;
}
</style>