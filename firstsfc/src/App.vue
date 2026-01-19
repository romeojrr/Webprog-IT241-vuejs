<template>
  <div id="app">
    <personal-profile />

    <div class="container py-5">
      <h2 class="text-center mb-4">My Favorite Foods</h2>
      <div class="d-flex justify-content-center gap-3">
        <food-item />
        <food-item2 />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>  