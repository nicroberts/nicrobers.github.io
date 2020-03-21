<template>
  <main-layout>
    <p>Work page</p>
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
    background: green;
  }

</style>
