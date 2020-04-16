<template>
  <main-layout>
    <Nav />
    <PageHeading 
      :title="'About.'"
      :sub="'Senior Designer with over 8 years experience designing for ecommerce brands, publication houses and design agencies.'"
      :para="'With my experience of designing in house for large fashion and lifestyle brands and my knowledge of ecommerce as a whole, I am greatly successful at designing effective solutions that have proved their value whilst taking into account the business needs and priorities.  I have a diverse background of experience and always excited by new and interesting projects.'"
      :bg="'#fff'"
    />

    <ImageCopy 
      :right="false"
      :imageBg="'#CDC6BE'"
      :image="require('../images/me.jpg')"
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

    <Footer />

  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import PageHeading from '../components/PageHeading.vue'
  import ImageCopy from '../components/ImageCopy.vue'
  import ScrollList from '../components/ScrollList.vue'
  import Footer from '../components/Footer.vue'


  export default {
    data: function () {
      return {
        
      }
    },
    components: {
      MainLayout, PageHeading, Nav, ImageCopy, ScrollList, Footer
    }
  }
</script>

<style scoped>



</style>