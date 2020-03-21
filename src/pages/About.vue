<template>
  <main-layout>
    <p>About page</p>
  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'

  export default {
    components: {
      MainLayout
    }
  }
</script>

<style scoped>

  p {
    height: 100vh;
    width: 100%;
    background: red;
  }

</style>