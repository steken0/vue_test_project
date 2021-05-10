<template>
    <button @click="onClick()">
        {{text}}
    </button>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
    name: "Button",
    methods: {
        onClick() {
            console.log("Clicked me beach")
        }
    },
    props: {
        text: {
            type: String,
            default: "Click me"
        }
    }
})
</script>

<style scoped>
    button {
        background-color:steelblue;
        color: white;
    }
</style>