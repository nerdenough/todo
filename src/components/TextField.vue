<template>
  <input class="text-field" type="text" placeholder="Add a Todo" />
</template>

<script>
export default {
  name: 'text-field',
  components: {
  }
};
</script>

<style scoped>
.text-field {
  background: #AED581;
  color: white;
  font-size: 18px;
  width: 100%;
  height: 100%;
  border: none;
  outline: none;
  padding: 0 15px;
  box-sizing: border-box;
}

.text-field::placeholder {
  color: #DCEDC8;
}
</style>
