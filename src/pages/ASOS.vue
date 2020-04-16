<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'ASOS.'"
      :categories="'UI DESIGN  |  UX DESIGN  |  APP DESIGN  |  ICONOGRAPHY'"
      :sub="'AR make-up app design.'"
      :para="'Augmented reality Make-up App design to co-inside with the launch of ASOS’s new beauty range.  Working with a 3rd party, I lead the design and enhancement of their existing technology to build a bespoke experience for ASOS.'"
      :bg="'#fff'"
    />

    <FullImage 
      :images="imageArray"
      :bg="'#C8C1BB'"
    />

    <ImageCopy 
      :right="false"
      :imageBg="'#E2DCD4'"
      :image="require('../images/asos-approach.jpg')"
      :head="'The Approach.'"
      :text="'Starting completely from scratch from the user journey, wireframes and finally the applied UI, ensuring a clean and simple experience for the user.'"
    />

    <PageHeading 
      :sub="'Simplifying the UI design, creating a well designed and easy to use interface.'"
      :para="'Icons where very important in this project, being that there had to be around 30, each had to remain clear at small sizes and feel ASOS branded.  The focus of the UI had to be the camera element, so although important the menu needed to remain understated and easy to use.'"
      :bg="'#fff'"
    />

    <FullImage 
      :images="imageArrayTwo"
      :bg="'#C8C1BB'"
    />

    <ImageCopy 
      :right="true"
      :alt="true"
      :imageBg="'#E2DCD4'"
      :image="require('../images/asos-purchase.png')"
      :head="'Saved and pre-loaded looks.'"
      :text="'To enhance the shopping experience of the app, both curated content and the ability to save user generated content had to be integrated into the experience.  Pre-loaded looks and saved looks really enhance the experience to encourage users to return and always feel there is fresh content.'"
      :headTwo="'Scan products.'"
      :textTwo="'Functionality that allowed users to scan the barcode of beauty products meant the app could be integrated into the customers everyday when it came to selecting beauty products.  Users were able to try on multipul products and purchase at the tap of a button.'"
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
            src: require('../images/asos-drop-down.jpg'),
            alt: "ASOS drop down"
          },
          {
            src: require('../images/asos-firstscreen.jpg'),
            alt: "ASOS first screen"
          },
          {
            src: require('../images/asos-eyes.jpg'),
            alt: "ASOS eyes"
          },
          {
            src: require('../images/asos-application.jpg'),
            alt: "ASOS application"
          },
          {
            src: require('../images/asos-colour.jpg'),
            alt: "ASOS colour"
          },
          {
            src: require('../images/asos-overlay.jpg'),
            alt: "ASOS overlay"
          }
        ],  
        imageArrayTwo: [
          {
            src: require('../images/asos-drop-down.jpg'),
            alt: "ASOS drop down"
          },
          {
            src: require('../images/asos-complete.jpg'),
            alt: "ASOS complete looks"
          },
          {
            src: require('../images/asos-saved.jpg'),
            alt: "ASOS saved looks"
          },
          {
            src: require('../images/asos-look1.jpg'),
            alt: "ASOS look 1"
          },
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
