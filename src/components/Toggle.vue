<script setup>
import { defineAsyncComponent, ref } from 'vue';
import AsyncComponent from './AsyncComponent.vue';

const showComp = ref(false)

</script>
<template>
    <div v-if="showComp">
      <AsyncComponent />
    </div>
    <button @click="showComp = !showComp">Toggle</button>
</template>
