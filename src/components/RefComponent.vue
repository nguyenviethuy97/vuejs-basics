<script setup>
import BasicRef from './BasicRef.vue';

import { ref, onMounted } from 'vue';
const myRef = ref(null)

onMounted(() => {
  console.log('::HERE',myRef.value.myFunction())
})

</script>
<template>
  <BasicRef ref="myRef"/>
</template>
