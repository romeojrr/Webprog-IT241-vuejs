<template>
  <div>
    <div class="banana">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Banana Lover 67',
      message: 'Chimpanzini Bananini'
    }
  }
};
</script>

<style>
    .banana {
    border: dotted 1.5px;
    border-radius: 6px;
    display: inline-block;
    margin: 10px;
    padding: 15px;
    background-color: yellow;
  }
</style>