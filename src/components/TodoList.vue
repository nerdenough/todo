<template>
  <div class="todo-list">
    <div class="todo-item" v-for="todo in todos">
      <div class="text">{{ todo }}</div>
      <button class="delete" @click="removeTodo(todos, todo)"><i class="fa fa-trash"></i></button>
    </div>
  </div>
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
.todo-list {
  width: 100%;
  padding-bottom: 10px;
}

.todo-item {
  display: flex;
  padding: 10px;
  padding-bottom: 0;
}

.text {
  flex-grow: 1;
  background: white;
  color: #808080;
  padding: 20px 15px;
  border-right: none;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
}

.delete {
  background: #E91E63;
  color: white;
  font-size: 18px;
  padding: 10px 20px;
  border: none;
  outline: none;
  cursor: pointer;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}

.delete:hover {
  background: #F06292;
}
</style>
