<template>
  <div class="todo-header">
    <input v-model="todo" class="text-field" type="text" placeholder="Add a Todo" />
    <button @click="addTodo(todos, todo)" class="add-button"><i class="fa fa-plus"></i> Todo</button>
  </div>
</template>

<script>
export default {
  name: 'todo-header',
  data: () => {
    return {
      todo: ''
    };
  },
  props: {
    todos: {
      type: Array,
      required: true
    },
    addTodo: {
      type: Function,
      required: true
    }
  }
};
</script>

<style scoped>
.todo-header {
  display: flex;
  width: 100%;
  height: 80px;
  background: #8BC34A;
  padding: 10px;
  box-sizing: border-box;
}

.text-field {
  flex-grow: 1;
  height: 100%;
  background: #AED581;
  color: white;
  font-size: 18px;
  border: none;
  outline: none;
  padding: 0 15px;
  box-sizing: border-box;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
}

.text-field::placeholder {
  color: #DCEDC8;
}

.add-button {
  height: 100%;
  background: white;
  color: #8BC34A;
  font-size: 18px;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 0 15px;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
  box-sizing: border-box;
}

.add-button:hover {
  background: #DCEDC8;
}
</style>
