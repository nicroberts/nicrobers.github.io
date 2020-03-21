<template>
  <main-layout>
    <Nav />
    <p>Work page</p>
  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'

  export default {
    components: {
      MainLayout, Nav
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
