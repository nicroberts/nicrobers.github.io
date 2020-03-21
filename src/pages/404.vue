<template>
  <main-layout>
    <Nav />
    <p>Page not found</p>
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
