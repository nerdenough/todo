<template>
  <div class="todo-list">
    <transition-group name="fade">
      <div class="todo-item" v-for="todo in todos" :key="todo">
        <div class="text">{{ todo }}</div>
        <button class="delete" @click="removeTodo(todos, todo)"><i class="fa fa-trash"></i></button>
      </div>
    </transition-group>
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
  max-width: 100%;
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
  overflow: hidden;
}

.delete {
  flex-basis: 0;
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

.fade-enter-active, .fade-leave-active {
  transition: opacity ease-in-out .2s
}
.fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0
}
</style>
