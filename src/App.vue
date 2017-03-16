<template>
  <div class="app">
    <todo-header :todos="todos" :addTodo="addTodo" />
    <todo-list :todos="todos" :removeTodo="removeTodo" />
  </div>
</template>

<script>
import TodoHeader from './components/TodoHeader';
import TodoList from './components/TodoList';

export default {
  name: 'app',
  components: {
    TodoHeader,
    TodoList
  },
  data: () => {
    return {
      todos: []
    };
  },
  methods: {
    addTodo: (todos, todo) => {
      if (todo) {
        todos.splice(0, 0, todo);
      }
    },
    removeTodo: (todos, todo) => {
      todos.splice(todos.indexOf(todo), 1);
    }
  }
};
</script>

<style>
html, body {
  background: #F5F5F5;
  font-family: 'Noto Sans', sans-serif;
  margin: 0;
}
</style>
