<template>
  <header>
    <h1>Task Tracker</h1>

    <VueButton 
      @btn-click="$emit('toggle-add-task')" 
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
    <!-- <VueButton text="Update Task" color="blue"/> -->
    <!-- <VueButton text="Delete Task" color="red"/> -->
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
    },
    showAddTask: Boolean,
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