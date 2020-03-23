<template>
  <main-layout>
    <Nav />
   <div class="container home">
    <div class="row">
      <div class="col-1 hidden-sm"></div>
      <div class="col-10">
        <a href="/topshop">Welcome home</a>

      </div>
    </div>
  </div>
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
    background: #F2F2F2;
  }

  .container.home {
    background: #F2F2F2;
  }

</style>
