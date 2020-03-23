<template>
  <main-layout>
    <Nav />
      <PageHeading 
      :title="'Topshop.'"
      :para="'Responsive site redesign of Topshop.com, focusing on improving the experience of the shopping journey including product listing pages, product description pages, bag drawer and menus.'"
      :bg="'#fff'"
    />

     <ImageCopy 
      :right="false"
      :image="'https://i.ytimg.com/vi/z1rtviBRNTw/maxresdefault.jpg'"
      :head="'The Approach.'"
      :text="'Mobile first approach to all pages, simplifying and cleaning up pages.  Introducing intuitive swipes and expanding accordions, but focusing on immersive imagery and dynamic pages.'"
    />

    <PageHeading 
      :sub="'Dynamic image focused product listing pages.'"
      :para="'Image is key for topshop.com, so working with the Art Director we established a fresher feeling page by introducing more types of shots to the product photography.  Creating different experiences across devices allows a truly tailored experience for the customer.'"
      :bg="'#fff'"
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
      MainLayout, PageHeading, Nav, ImageCopy,
    }
  }
</script>

<style scoped>



</style>
