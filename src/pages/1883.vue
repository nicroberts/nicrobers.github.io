<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'1883 Magazine.'"
      :categories="'PUBLICATION DESIGN   |   PRINT DESIGN'"
      :sub="'Magazine Issue ?.'"
      :para="'Online shoppable lookbook design for Warehouse AW14 Collection. The desktop design offers an easily navigated lookbook that once interacted with, splits into detailed product imagery with the ability to add products directly to bag.'"
      :bg="'#fff'"
    />
    
    <FullImage 
      :images="ImageArray"
      :bg="'#AB9389'"
    />

    <ImageCopy 
      :right="false"
      :imageBg="'#E2DCD4'"
      :image="require('../images/18832.jpg')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

   <TwoCentredImages 
      :images="ImageArrayTwo"
      :bg="'#AB9389'"
      :bottomLeft="false"
      :bottomRight="false"
     />

    <PageHeading 
      :sub="'Simplifying the UI design, creating a well designed and easy to use interface.'"
      :para="'Icons where very important in this project, being that there had to be around 30, each had to remain clear at small sizes and feel ASOS branded.  The focus of the UI had to be the camera element, so although important the menu needed to remain understated and easy to use.'"
      :bg="'#fff'"
    />

    <FullImage 
      :images="ImageArrayThree"
      :bg="'#E2DCD4'"
    />

   <NextProject
      :title="'Topshop.'"
      :categories="'UI DESIGN | UX DESIGN | VISUAL IDENTITY'"
      :sub="'Next project.'"
      :bg="'#fff'"
      :link="'/topshop'"
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
            src: require('../images/18831.jpg'),
            alt: "Warehouse lookbook"
          },
        ],  
        ImageArrayTwo: [
          {
            src: require('../images/18833.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/18834.jpg'),
            alt: "Warehouse lookbook"
          }
        ],
        ImageArrayThree: [
          {
            src: require('../images/18835.jpg'),
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
