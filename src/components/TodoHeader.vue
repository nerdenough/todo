<template>
  <div class="todo-header">
    <text-field />
  </div>
</template>

<script>
import TextField from './TextField';

export default {
  name: 'todo-header',
  components: {
    TextField
  }
};
</script>

<style scoped>
.todo-header {
  width: 100%;
  height: 80px;
  background: #8BC34A;
  padding: 10px;
  box-sizing: border-box;
}
</style>
