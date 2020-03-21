<template>
  <main-layout>
   <div class="container home">
    <div class="row">
      <div class="col-1 hidden-sm"></div>
      <div class="col-10">
        <p>Welcome home</p>
      </div>
    </div>
  </div>
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
    background: blue;
  }

</style>
