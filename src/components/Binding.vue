<template>
  <div>
    <h1 :id="id">Binding property here</h1>
    <input type="text" :disabled="isDisabled">
    <button @click="isDisabled = !isDisabled">Lock</button>

    <h2 :class="{chosen: isSelected}">Binding class</h2>
    <button @click="isSelected = !isSelected">Change</button>

    
    <form>
      <input type="text" v-model="changeName">
      <button @click.prevent="changeName = 'abc'">Click</button>
    </form>

    <div v-show="isShow">V-show/hide</div>
    
    <div v-if="isShow">V-if</div>
    <button @click="isShow=!isShow">
      <span v-if="isShow">Hide</span>
      <span v-else>Show</span>
    </button>

    
</div>
</template>

<script>
export default {
  data: () => {
    return {
      id: '123',
      isDisabled: true,
      isSelected: true,
      changeName: 'tuwnguyen',
      isShow: true,
    }
  }
}
</script>

<style>
.chosen {
  color: red;
}
</style>