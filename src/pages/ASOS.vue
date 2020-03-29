<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'ASOS.'"
      :categories="'UI DESIGN | UX DESIGN | VISUAL IDENTITY'"
      :sub="'Website redesign.'"
      :para="'Responsive site redesign of Topshop.com, focusing on improving the experience of the shopping journey including product listing pages, product description pages, bag drawer and menus.'"
      :bg="'red'"
    />

    <FullImage 
      :images="imageArraySix"
      :bg="'blue'"
    />

    <FullImage 
      :images="imageArrayFour"
      :bg="'#CDB5A6'"
    />

    

  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import ProjectHeading from '../components/ProjectHeading.vue'
  import FullImage from '../components/FullImage.vue'

  export default {

    data: function () {
      return {
          imageArraySix: [
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            }
          ],
          imageArrayFour: [
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-filters.jpg'),
              alt: "ASOS drop down"
            }
          ],
      }
    },

    components: {
      MainLayout, Nav, ProjectHeading, FullImage
    }
  }
</script>

<style scoped>



</style>
