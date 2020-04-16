<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'Netflix.'"
      :categories="'UI DESIGN   |   UX DESIGN'"
      :sub="'Stranger Things x Topshop.'"
      :para="'Online shoppable lookbook design for Warehouse AW14 Collection. The desktop design offers an easily navigated lookbook that once interacted with, splits into detailed product imagery with the ability to add products directly to bag.'"
      :bg="'#fff'"
    />
    
    <FullImage 
      :images="ImageArray"
      :bg="'#B7B6BB'"
    />

    <ImageCopy 
      :right="false"
      :imageBg="'#C8C1BB'"
      :image="require('../images/Netflix5.jpg')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

    <PageHeading 
      :sub="'Simplifying the UI design, creating a well designed and easy to use interface.'"
      :para="'Icons where very important in this project, being that there had to be around 30, each had to remain clear at small sizes and feel ASOS branded.  The focus of the UI had to be the camera element, so although important the menu needed to remain understated and easy to use.'"
      :bg="'#fff'"
    />

   <TwoCentredImages 
      :images="ImageArrayTwo"
      :bg="'#B7B6BB'"
      :bottomLeft="false"
      :bottomRight="false"
     />

   <NextProject
      :title="'1883 Magazine.'"
      :categories="'PUBLICATION DESIGN | PRINT DESIGN'"
      :sub="'Next project.'"
      :bg="'#fff'"
      :link="'/1883'"
    />

  <Footer />    

  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import ProjectHeading from '../components/ProjectHeading.vue'
  import ImageCopy from '../components/ImageCopy.vue'
  import FullImage from '../components/FullImage.vue'
  import PageHeading from '../components/PageHeading.vue'
  import TwoCentredImages from '../components/TwoCentredImages.vue'
  import NextProject from '../components/NextProject.vue'
  import Footer from '../components/Footer.vue'

  export default {

    data: function () {
      return {
        ImageArray: [
          {
            src: require('../images/Netflix1.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/Netflix2.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/Netflix3.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/Netflix4.jpg'),
            alt: "Warehouse lookbook"
          }
        ],  
        ImageArrayTwo: [
          {
            src: require('../images/Netflix6.jpg'),
            alt: "Warehouse lookbook"
          },
         {
            src: require('../images/Netflix7.jpg'),
            alt: "Warehouse lookbook"
          }
        ],
      }
    },

    components: {
      MainLayout, Nav, ProjectHeading, TwoCentredImages, ImageCopy, FullImage, PageHeading, NextProject, Footer
    }
  }
</script>

<style scoped>



</style>
