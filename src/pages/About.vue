<template>
  <main-layout>
    <Nav />
    <PageHeading 
      :title="'About.'"
      :sub="'Uruoi concentrates on the core elements of skincare to combine an authentically Japanese minimalist philosophy and powerful ingredients backed by science.'"
      :para="'This project was all about minimalism. My main objective was to come up with a design to support brand’s philosophy as well as bring it to the digital world in the best shape. My main objective was to come up with a design to support brand’s philosophy as well as bring it to the digital world in the best shape.'"
      :bg="'#bada55'"
    />

    <ImageCopy 
      :right="false"
      :image="'https://i.ytimg.com/vi/z1rtviBRNTw/maxresdefault.jpg'"
      :head="'My Experience.'"
      :text="'I have a diverse range of experience in a number of different disciplinaries including UI and UX design, print and publication design and art direction.'"
    />
  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import PageHeading from '../components/PageHeading.vue'
  import ImageCopy from '../components/ImageCopy.vue'

  export default {
    components: {
      MainLayout, PageHeading, Nav, ImageCopy
    }
  }
</script>

<style scoped>



</style>