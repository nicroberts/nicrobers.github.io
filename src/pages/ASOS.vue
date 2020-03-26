<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'ASOS.'"
      :categories="'UI DESIGN | UX DESIGN | VISUAL IDENTITY'"
      :sub="'Website redesign.'"
      :para="'Responsive site redesign of Topshop.com, focusing on improving the experience of the shopping journey including product listing pages, product description pages, bag drawer and menus.'"
      :bg="'#fff'"
    />

    

  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import ProjectHeading from '../components/ProjectHeading.vue'

  export default {

    data: function () {
      return {
          
      }
    },

    components: {
      MainLayout, Nav, ProjectHeading
    }
  }
</script>

<style scoped>



</style>
