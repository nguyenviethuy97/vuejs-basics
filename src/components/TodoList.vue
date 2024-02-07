<template>
  <div>
    <div id="app">
      <input type="text" v-model="newTask">
      <button @click="addTask()">Add</button>
      <div v-for="task in tasks">
        <input type="checkbox" v-model="task.done">
        <span :class="{done: task.done}">{{ task.content }}</span>
      </div>
    </div>
</div>
</template>

<script>
export default {
  data: () => {
    return {
      newTask: '',
      tasks: []
    }
  },
  methods: {
    addTask: () => {
      this.tasks.push({content: this.newTask, done: false})
    }
  },
  watch: {
    newTask: (oldVal, newVal) => {
      console.log(oldVal, newVal)
    }
  }
}
</script>

<style>
.done {
  text-decoration: line-through;
}
</style>