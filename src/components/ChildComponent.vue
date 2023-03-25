<template>
<h1>Child Component</h1>
  <h2>Child Counter: {{ this.childCounter }}</h2>
  <button @click="addNumber">
    increment child counter
  </button>
</template>

<script>
export default {
name: "ChildComponent",
  data() {
    return {
      childCounter: 0,
    }
  },
  methods: {
    addNumber(){
      this.childCounter ++;
    }
  },
}
</script>

<style scoped>

</style>