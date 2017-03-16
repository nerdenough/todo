<template>
  <div class="app">
    <todo-header :todos="todos" :addTodo="addTodo" />
    <ul>
      <li v-for="todo in todos">{{ todo }}</li>
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
    }
  }
};
</script>

<style>
html, body {
  margin: 0;
}
</style>
