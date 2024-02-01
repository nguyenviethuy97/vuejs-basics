<template>
  <div>
    <div v-show="isShow">
      <h1>Test hide/show element</h1>
    </div>
    <button @click="isShow=!isShow">Hide/Show</button>
</div>
</template>

<script>
export default {
  data: () => {
    return {
      isShow: true
    }
  }
}
</script>