<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld :msg="msg"/>
  <InputTest />
  <Binding/>
  <TodoList/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import InputTest from './components/InputTest.vue'
import Binding from './components/Binding.vue'
import TodoList from './components/TodoList.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    InputTest,
    Binding,
    TodoList,
  },
  data: () => {
    return {
      msg: "Welcome to Your Vue.js App"
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
