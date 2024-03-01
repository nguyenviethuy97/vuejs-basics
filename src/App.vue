<template>
  <img alt="Vue logo" src="./assets/logo.png">
    <div v-if="false">
      <HelloWorld :msg="msg"/>
      <InputTest />
      <Binding/>
      <TodoList/>
      <SlotComponent>
        <h1>Content 1</h1>
        <h1>Content 2</h1>
      </SlotComponent>
      <FallbackSlotContent>
        <!-- <h1>Not default content</h1> -->
      </FallbackSlotContent>
      <NamedSlot>
        <template v-slot:one>
          <h1> This slot go to content 1</h1>
        </template>
        <template #two>
          <h1> This slot go to content 2</h1>
        </template>
      </NamedSlot>
      <BasicRef></BasicRef>
      <RefComponent></RefComponent>
      <Toggle></Toggle>
    </div>
  <DynamicComponent></DynamicComponent>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import InputTest from './components/InputTest.vue'
import Binding from './components/Binding.vue'
import TodoList from './components/TodoList.vue'
import SlotComponent from './components/SlotComponent.vue'
import FallbackSlotContent from './components/FallbackSlotContent.vue'
import NamedSlot from './components/NamedSlot.vue'
import BasicRef from './components/BasicRef.vue'
import RefComponent from './components/RefComponent.vue'
import Toggle from './components/Toggle.vue'
import DynamicComponent from './components/DynamicComponent.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    InputTest,
    Binding,
    TodoList,
    SlotComponent,
    FallbackSlotContent,
    NamedSlot,
    BasicRef,
    RefComponent,
    Toggle,
    DynamicComponent
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
