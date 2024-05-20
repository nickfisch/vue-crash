<template>
  <div v-for="task in tasks" :key="task.id">
    <TaskItem :task="task"/>
  </div>
</template>

<script>
  import TaskItem from './TaskItem';

  export default {
    name: 'TasksList',
    props: {
      tasks: Array
    },
    components: {
      TaskItem,
    }
  }
</script>

<style>
</style>