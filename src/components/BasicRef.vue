<script setup>
import { ref, onMounted, defineExpose } from 'vue';
const myRef = ref('')
const num = ref(0)
const myFunction = () => {
  return true
}
defineExpose({myRef, num, myFunction})
// function ref
const myRefFunc = (el) => {
  console.log(el.textContent)
  el.textContent = "My Function Ref"
}

onMounted(() => {
  console.log(myRef.value)
  myRef.value.focus()
})

</script>
<template>
  <input type="text" name="name" ref="myRef">
  <p :ref="myRefFunc">Normal text</p>
</template>
