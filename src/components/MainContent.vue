<template>
  <div class="main-content"></div>
</template>

<script>
export default {
  name: 'MainContent'
}
</script>

<style scoped>
  .main-content {
    display: grid;
    grid-template-columns: 400px 400px;
    grid-auto-rows: 400px 400px;
  }
</style>
