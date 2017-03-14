<template>
  <button @click="onClick" class="add-button">Add</button>
</template>

<script>
export default {
  name: 'add-button',
  methods: {
    onClick: () => {
      console.log('Add todo!!!!');
    }
  }
};
</script>

<style scoped>
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
