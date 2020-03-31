<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'Rollacoaster.'"
      :categories="'PUBLICATION DESIGN   |   PRINT DESIGN'"
      :sub="'Magazine Issue 8.'"
      :para="'Online shoppable lookbook design for Warehouse AW14 Collection. The desktop design offers an easily navigated lookbook that once interacted with, splits into detailed product imagery with the ability to add products directly to bag.'"
      :bg="'#fff'"
    />

    <TwoCentredImages 
      :images="ImageArray"
      :bg="'#CDC7C0'"
      :bottomLeft="false"
      :bottomRight="false"
     />

    <ImageCopy 
      :right="false"
      :imageBg="'#EEEDE5'"
      :image="require('../images/rollacoaster3.jpg')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

   <TwoCentredImages 
      :images="ImageArrayTwo"
      :bg="'#CDC7C0'"
      :bottomLeft="false"
      :bottomRight="false"
     />

    <PageHeading 
      :sub="'Simplifying the UI design, creating a well designed and easy to use interface.'"
      :para="'Icons where very important in this project, being that there had to be around 30, each had to remain clear at small sizes and feel ASOS branded.  The focus of the UI had to be the camera element, so although important the menu needed to remain understated and easy to use.'"
      :bg="'#fff'"
    />

   <TwoCentredImages 
      :images="ImageArrayThree"
      :bg="'#EEEDE5'"
      :bottomLeft="false"
      :bottomRight="false"
     />

    <ImageCopy 
      :right="true"
      :alt="true"
      :imageBg="'#CDC7C0'"
      :image="require('../images/rollacoaster8.jpg')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

   <NextProject
      :title="'Topshop.'"
      :categories="'UI DESIGN | UX DESIGN | VISUAL IDENTITY'"
      :sub="'Next project.'"
      :bg="'#fff'"
    />

    

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

  export default {

    data: function () {
      return {
        ImageArray: [
          {
            src: require('../images/rollacoaster1.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/rollacoaster2.jpg'),
            alt: "Warehouse lookbook"
          }
        ],  
        ImageArrayTwo: [
          {
            src: require('../images/rollacoaster4.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/rollacoaster5.jpg'),
            alt: "Warehouse lookbook"
          }
        ],
        ImageArrayThree: [
          {
            src: require('../images/rollacoaster6.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/rollacoaster7.jpg'),
            alt: "Warehouse lookbook"
          }
        ], 
      }
    },

    components: {
      MainLayout, Nav, ProjectHeading, TwoCentredImages, ImageCopy, FullImage, PageHeading, NextProject
    }
  }
</script>

<style scoped>



</style>
