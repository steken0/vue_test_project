<template>
  <div class="home">
    <Button text="Epic toggle button"/>
    <Tasks :tasks="tasks" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Button from '@/components/Button.vue'
import Tasks from '@/components/Tasks.vue'

export interface task {
  id: number,
  text: string
}

export default defineComponent({
  name: "Home",
  components: {
    Button,
    Tasks
  },
  data() {
    return {
      tasks: Array<task>()
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: "Get a drink",
      },
      {
        id: 2,
        text: "Go to the movies",
      },
      {
        id: 3,
        text: "Go to sleep",
      }
    ]
    console.log(this.tasks)
  }
});
</script>
