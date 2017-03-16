<template>
  <div class="app">
    <todo-header :todos="todos" :addTodo="addTodo" />
    <ul>
      <li v-for="todo in todos">
        {{ todo }}
        <button @click="removeTodo(todos, todo)">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script>
import TodoHeader from './components/TodoHeader';

export default {
  name: 'app',
  components: {
    TodoHeader
  },
  data: () => {
    return {
      todos: []
    };
  },
  methods: {
    addTodo: (todos, todo) => {
      todos.push(todo);
    },
    removeTodo: (todos, todo) => {
      todos.splice(todos.indexOf(todo), 1);
    }
  }
};
</script>

<style>
html, body {
  margin: 0;
}
</style>
