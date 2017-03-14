<template>
  <div class="todo-header">
    <text-field />
    <add-button />
  </div>
</template>

<script>
import AddButton from './AddButton';
import TextField from './TextField';

export default {
  name: 'todo-header',
  components: {
    AddButton,
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
