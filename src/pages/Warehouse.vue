<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'Warehouse.'"
      :categories="'UI DESIGN  |  UX DESIGN'"
      :sub="'Lookbook feature.'"
      :para="'Online shoppable lookbook design for Warehouse AW14 Collection. The desktop design offers an easily navigated lookbook that once interacted with, splits into detailed product imagery with the ability to add products directly to bag.'"
      :bg="'#fff'"
    />

    <FullImage 
      :images="imageArray"
      :bg="'#B7B6BB'"
    />

    <ImageCopy 
      :right="false"
      :imageBg="'#AB9389'"
      :image="require('../images/warehouse-lookbook-mob.jpg')"
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

    <ImageCopy 
      :right="true"
      :alt="true"
      :imageBg="'#AB9389'"
      :image="require('../images/warehouse-lookbook-mobiles.png')"
      :head="'Saved and pre-loaded looks.'"
      :text="'To enhance the shopping experience of the app, both curated content and the ability to save user generated content had to be integrated into the experience.  Pre-loaded looks and saved looks really enhance the experience to encourage users to return and always feel there is fresh content.'"
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
  import TwoCentredImages from '../components/TwoCentredImages.vue'
  import FullImage from '../components/FullImage.vue'
  import PageHeading from '../components/PageHeading.vue'
  import NextProject from '../components/NextProject.vue'

  export default {

    data: function () {
      return {
        imageArray: [
          {
            src: require('../images/warehouse-lookbook.jpg'),
            alt: "Warehouse lookbook"
          }
        ],  
        ImageArrayTwo: [
          {
            src: require('../images/warehouse-lookbook-2.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/warehouse-lookbook-3.jpg'),
            alt: "Warehouse lookbook"
          },
        ]   
      }
    },

    components: {
      MainLayout, Nav, ProjectHeading, ImageCopy, FullImage, PageHeading, TwoCentredImages, NextProject
    }
  }
</script>

<style scoped>



</style>
