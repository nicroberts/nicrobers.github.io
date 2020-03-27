<template>
  <main-layout>
    <Nav />

    <ProjectHeading 
      :title="'Topshop.'"
      :categories="'UI DESIGN | UX DESIGN | VISUAL IDENTITY'"
      :sub="'Website redesign.'"
      :para="'Responsive site redesign of Topshop.com, focusing on improving the experience of the shopping journey including product listing pages, product description pages, bag drawer and menus.'"
      :bg="'#fff'"
    />

    <TwoCentredImages 
      :images="PLPImageArray"
      :bg="'#3F3F3F'"
      :bottomLeft="true"
      :bottomRight="false"
     />

    <ImageCopy 
      :right="false"
      :alt="true"
      :imageBg="'#CDC6BE'"
      :image="require('../images/topshop-image.jpg')"
      :head="'The Approach.'"
      :text="'Mobile first approach to all pages, simplifying and cleaning up pages.  Introducing intuitive swipes and expanding accordions, but focusing on immersive imagery and dynamic pages.'"
      :headTwo="'The Approach.'"
      :textTwo="'Mobile first approach to all pages, simplifying and cleaning up pages.  Introducing intuitive swipes and expanding accordions, but focusing on immersive imagery and dynamic pages.'"
    />

    <TwoCentredImages 
      :images="PLPImageArray"
      :bg="'#3F3F3F'"
      :bottomLeft="true"
      :bottomRight="false"
     />

    <PageHeading 
      :sub="'Dynamic image focused product listing pages.'"
      :para="'Image is key for topshop.com, so working with the Art Director we established a fresher feeling page by introducing more types of shots to the product photography.  Creating different experiences across devices allows a truly tailored experience for the customer.'"
      :bg="'#fff'"
    />

      <TwoCentredImages 
      :images="PDPImageArray"
      :bg="'#CDC6BE'"
      :bottomLeft="false"
      :bottomRight="false"
     />

    <PageHeading 
      :sub="'Dynamic image focused product listing pages.'"
      :para="'Image is key for topshop.com, so working with the Art Director we established a fresher feeling page by introducing more types of shots to the product photography.  Creating different experiences across devices allows a truly tailored experience for the customer.'"
      :bg="'#fff'"
    />

    <ImageCopy 
      :right="true"
      :imageBg="'#CDC6BE'"
      :image="require('../images/topshop-image.jpg')"
      :head="'The Approach.'"
      :text="'Mobile first approach to all pages, simplifying and cleaning up pages.  Introducing intuitive swipes and expanding accordions, but focusing on immersive imagery and dynamic pages.'"
    />

    <FullImage 
      :images="imageArray"
      :bg="'#CDC6BE'"
    />

    <NextProject
      :title="'ASOS.'"
      :categories="'UI DESIGN | UX DESIGN | VISUAL IDENTITY'"
      :sub="'Next project.'"
      :bg="'#fff'"
    />

  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'
  import PageHeading from '../components/PageHeading.vue'
  import ProjectHeading from '../components/ProjectHeading.vue'
  import ImageCopy from '../components/ImageCopy.vue'
  import FullImage from '../components/FullImage.vue'
  import TwoCentredImages from '../components/TwoCentredImages.vue'
  import NextProject from '../components/NextProject.vue'

  export default {

    data: function () {
      return {
          imageArray: [
            {
              src: require('../images/topshop-plp-nav.png'),
              alt: "ASOS drop down"
            }
          ],
          PLPImageArray: [
            {
              src: require('../images/topshop-plp-desktop.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-plp-mob.png'),
              alt: "ASOS drop down"
            }
          ],
          PDPImageArray: [
            {
              src: require('../images/topshop-pdp-dekstop.jpg'),
              alt: "ASOS drop down"
            },
            {
              src: require('../images/topshop-pdp-mob.jpg'),
              alt: "ASOS drop down"
            }
          ]
      }
    },

    components: {
      MainLayout, PageHeading, Nav, ImageCopy, FullImage, TwoCentredImages, ProjectHeading, NextProject
    }
  }
</script>

<style scoped>



</style>
