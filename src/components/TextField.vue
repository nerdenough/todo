<template>
  <input class="text-field" type="text" placeholder="Add a Todo" />
</template>

<script>
export default {
  name: 'text-field'
};
</script>

<style scoped>
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
</style>
