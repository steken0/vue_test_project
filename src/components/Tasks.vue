<template>
    <h1>
        This is the tasks:
    </h1>
    <div :key="task.id" v-for="task in tasks">
        <h3>{{task.text}}</h3>
    </div>
</template>


<script>
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'Tasks',
    props: {
        tasks: Array
    }
})
</script>
