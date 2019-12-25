<template>

  <div>
    <p>Completed Tasks: {{tasks.filter(todo => {return todo.done === true}).length}}</p>
    <p>Pending Tasks: {{tasks.filter(todo => {return todo.done === false}).length}}</p>
     <Task class='ui centered card' v-for="task in tasks" v-bind:key="task.id" v-bind:task="task"></Task>
  </div>
</template>

<script>
import Task from './task.vue'
export default {
props: ['tasks'],

components: {
    Task
  }
}
</script>

<style>

</style>