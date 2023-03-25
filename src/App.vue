<template>
  <div class="divide">
    <div class="subDiv">
      <h1>Parent page</h1>
      <button @click="useRefToIncrementChildCounter">increment child counter from parent</button>
    </div>

    <div class="subDiv">
      <ChildComponent 
          ref="childRef"
      />
    </div>
    
  </div>

</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: {ChildComponent},
  data() {
    return {
      parentCounter: 0,
    }
  },
  methods: {
    useRefToIncrementChildCounter() {
      this.$refs.childRef.addNumber();
      this.parentCounter = this.$refs.childRef.childCounter;
    },
  },
}
</script>

<style scoped>

.divide {
  display: flex;
  flex-direction: row;
  column-gap: 20px;
}
.subDiv{
    border: 2px solid green;
  padding: 10px;
  }
</style>
