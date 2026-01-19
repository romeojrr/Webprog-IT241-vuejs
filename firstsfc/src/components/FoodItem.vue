<template>
  <div>
    <div class="matcha">
      <h2>{{ name }}</h2>
      <p>{{ message }}</p>
    </div>
  </div> </template>

<script>
export default {
  data() {
    return {
      name: 'Matcha and Mango',
      message: 'I like matcha and mango'
    }
  }
};
</script>

<style>
    .matcha {
    border: dotted 1.5px;
    border-radius: 6px;
    display: inline-block;
    margin: 10px;
    padding: 15px;
    background-color: green;
  }
</style>
