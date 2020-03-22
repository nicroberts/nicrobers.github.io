<template>
  <main-layout>
    <Nav />
    <PageHeading 
      :title="'About.'"
      :sub="'Uruoi concentrates on the core elements of skincare to combine an authentically Japanese minimalist philosophy and powerful ingredients backed by science.'"
      :para="'This project was all about minimalism. My main objective was to come up with a design to support brand’s philosophy as well as bring it to the digital world in the best shape. My main objective was to come up with a design to support brand’s philosophy as well as bring it to the digital world in the best shape.'"
      :bg="'#fff'"
    />

    <ImageCopy 
      :right="false"
      :image="'https://i.ytimg.com/vi/z1rtviBRNTw/maxresdefault.jpg'"
      :head="'My Experience.'"
      :text="'I have a diverse range of experience in a number of different disciplinaries including UI and UX design, print and publication design and art direction.'"
    />

    <PageHeading 
      :title="'Skills.'"
      :bg="'#fff'"
      :list="['UI / UX', 'Prototyping', 'Art Direction', 'Visual Design', 'Mobile and Web Design', 'HTML / CSS']"
      :listTwo="['Product Design', 'Video Editing / Animation', 'Iconography', 'Print / Packaging Design', 'Branding', 'Typography']"
    />

    <ScrollList 
      :title="'Clients.'"
      :bg="'#fff'"
      :brandList="['Rollacoaster', 'Harrods', 'Warehouse', 'Made.com', 'Netflix', 'POP Magazine', 'ASOS', 'Selfridges', 'Topshop', 'Topman', 'Velour Magazine', 'Ivy Park', '1883 Magazine', 'Rollacoaster', 'Harrods', 'Warehouse', 'Made.com', 'Netflix', 'POP Magazine', 'ASOS', 'Selfridges', 'Topshop', 'Topman', 'Velour Magazine', 'Ivy Park', '1883 Magazine']"
    />

  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import PageHeading from '../components/PageHeading.vue'
  import ImageCopy from '../components/ImageCopy.vue'
  import ScrollList from '../components/ScrollList.vue'

  export default {
    components: {
      MainLayout, PageHeading, Nav, ImageCopy, ScrollList
    }
  }
</script>

<style scoped>



</style>