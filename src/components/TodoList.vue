<template>
  <ul>
    <li v-for="todo in todos">
      {{ todo }}
      <button @click="removeTodo(todos, todo)">Delete</button>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'todo-list',
  props: {
    todos: {
      type: Array,
      required: true
    },
    removeTodo: {
      type: Function,
      required: true
    }
  }
};
</script>

<style scoped>
</style>
