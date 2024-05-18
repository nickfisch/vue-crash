<template>
  <header>
    <h1>Task Tracker</h1>

    <VueButton text="Add Task" color="green"/>
    <VueButton text="Update Task" color="blue"/>
    <VueButton text="Delete Task" color="red"/>
  </header>
</template>

<script>
import VueButton from './Button.vue'

export default {
  name: 'TaskHeader',
  props: {
    title: {
      type: String, 
      default: "Hello title"
    }
  },
  components: {
    VueButton,
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>