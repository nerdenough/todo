<template>
  <div class="app">
    <todo-header />
  </div>
</template>

<script>
import TodoHeader from './components/TodoHeader';

export default {
  name: 'app',
  components: {
    TodoHeader
  }
};
</script>

<style>
html, body {
  margin: 0;
}
</style>
