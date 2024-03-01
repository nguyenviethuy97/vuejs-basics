<template>
  <div>
    <component :is="tab[currentTab]"></component>
    <button @click="currentTab = `FirstComp`">Toggle 1st</button>
    <button @click="currentTab = `SecondComp`">Toggle 2nd</button>
  </div>
</template>
<script setup>
  import { ref } from 'vue'
  import FirstComponent from './FirstComponent.vue'
  import SecondComponent from './SecondComponent.vue'
  const currentTab = ref('FirstComp')
  const tab = {
    FirstComp: FirstComponent,
    SecondComp: SecondComponent,
  }
</script>