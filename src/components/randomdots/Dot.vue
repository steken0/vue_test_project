<template>
  <div :style="style"></div>
</template>

<script>
export default {
  name: "Dot",
  props: {
    data: Object,
  },
  data() {
    return {
      style: {
        borderRadius: "50%",
        border: `${this.data.size}px solid ${this.data.color}`,
        width: "0%",
        position: "absolute",
        top: this.data.top + "%",
        left: this.data.left + "%",
      },
    };
  },
};
</script>