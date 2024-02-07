<template>
  <div>
    <div id="app">
      <input type="text" v-model="newTask">
      <button @click="addTask()">Add</button>
      <div v-for="task in tasks">
        <input type="checkbox" v-model="task.done">
        <span :class="{done: task.done}">{{ task.content | filterTask }}</span>
      </div>
    </div>
</div>
</template>

<script>
import { computed } from 'vue'
export default {
  data: () => {
    return {
      newTask: '',
      tasks: [{content: 'anything', done: false}]
    }
  },
  methods: {
    addTask() {
      this.tasks.push({content: this.newTask, done: false})
    },
  },
  watch: {
    newTask: (oldVal, newVal) => {
      console.log(oldVal, newVal)
    }
  },
  setup(){
    const filterTask = computed(() => {
      return 'ss' + '##';
    })

    return {
      filterTask
    }
  }
}


</script>

<style>
.done {
  text-decoration: line-through;
}
</style>