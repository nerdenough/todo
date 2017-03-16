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
