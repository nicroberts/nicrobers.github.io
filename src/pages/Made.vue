<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'Made.com.'"
      :categories="'UI DESIGN  |  UX DESIGN   |  PRODUCT DESIGN'"
      :sub="'Wishlist functionality.'"
      :para="'Online shoppable lookbook design for Warehouse AW14 Collection. The desktop design offers an easily navigated lookbook that once interacted with, splits into detailed product imagery with the ability to add products directly to bag.'"
      :bg="'#fff'"
    />

    <FullImage 
      :images="imageArray"
      :bg="'#E3E4E8'"
    />

    <ImageCopy 
      :right="false"
      :imageBg="'#B7B6BB'"
      :image="require('../images/made-wishlist5.png')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

    <PageHeading 
      :sub="'Simplifying the UI design, creating a well designed and easy to use interface.'"
      :para="'Icons where very important in this project, being that there had to be around 30, each had to remain clear at small sizes and feel ASOS branded.  The focus of the UI had to be the camera element, so although important the menu needed to remain understated and easy to use.'"
      :bg="'#fff'"
    />

    <ImageCopy 
      :right="true"
      :alt="true"
      :imageBg="'#B7B6BB'"
      :image="require('../images/made-wishlist6.png')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

    <FullImage 
      :images="imageArrayTwo"
      :bg="'#E3E4E8'"
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
  import NextProject from '../components/NextProject.vue'

  export default {

    data: function () {
      return {
        imageArray: [
          {
            src: require('../images/made-wishlist1.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/made-wishlist2.jpg'),
            alt: "Warehouse lookbook"
          },
         {
            src: require('../images/made-wishlist3.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/made-wishlist4.jpg'),
            alt: "Warehouse lookbook"
          }
        ],  
        imageArrayTwo: [
          {
            src: require('../images/made-wishlist7.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/made-wishlist8.jpg'),
            alt: "Warehouse lookbook"
          },
         {
            src: require('../images/made-wishlist9.jpg'),
            alt: "Warehouse lookbook"
          },
          {
            src: require('../images/made-wishlist10.jpg'),
            alt: "Warehouse lookbook"
          }
        ] 
      }
    },

    components: {
      MainLayout, Nav, ProjectHeading, ImageCopy, FullImage, PageHeading, NextProject
    }
  }
</script>

<style scoped>



</style>
