<template>
  <main-layout>
    <Nav />
    <div class="work" :class="{asos: asosHover, topshop: topshopHover, made: madeHover, warehouse: warehousepHover, rollacoaster: rollacoasterHover, selfridges: selfridgesHover, harrods: harrodsHover, netflix: netflixHover, magazine: magazineHover}">
    <div class="container">
      <div class="row">
        <div class="col-1 hidden-sm"></div>
        <div class="col-10">
          <h1>Work.</h1>
           <ul>
            <li id="asos" @mouseover="asosHover = true" @mouseleave="asosHover = false">ASOS.</li>
            <li id="topshop" @mouseover="topshopHover = true" @mouseleave="topshopHover = false">Topshop.</li>
            <li id="made" @mouseover="madeHover = true" @mouseleave="madeHover = false">Made.com.</li>
            <li id="warehouse" @mouseover="warehousepHover = true" @mouseleave="warehousepHover = false">Warehouse.</li>
            <li id="rollacoaster" @mouseover="rollacoasterHover = true" @mouseleave="rollacoasterHover = false">Rollacoaster.</li>
            <li id="selfridges" @mouseover="selfridgesHover = true" @mouseleave="selfridgesHover = false">Selfridges.</li>
            <li id="harrods" @mouseover="harrodsHover = true" @mouseleave="harrodsHover = false">Harrods.</li>
            <li id="netflix" @mouseover="netflixHover = true" @mouseleave="netflixHover = false">Netflix.</li>
            <li id="magazine" @mouseover="magazineHover = true" @mouseleave="magazineHover = false">1883 Magazine.</li>
          </ul> 
           <img class="image imageasos hidden" src="../images/hp-image-1.jpg" alt="examples of asos work" >
           <img class="image imagetopshop hidden" src="../images/hp-image-1.jpg" alt="examples of topshop work" >
           <img class="image imagemade hidden" src="../images/hp-image-1.jpg" alt="examples of made work" >
           <img class="image imagewarehouse hidden" src="../images/hp-image-1.jpg" alt="examples of warehouse work" >
           <img class="image imagerollacoaster hidden" src="../images/hp-image-1.jpg" alt="examples of rollacoaster work" >
           <img class="image imageselfridges hidden" src="../images/hp-image-1.jpg" alt="examples of selfridges work" >
           <img class="image imageharrods hidden" src="../images/hp-image-1.jpg" alt="examples of harrods work" >
           <img class="image imagenetflix hidden" src="../images/hp-image-1.jpg" alt="examples of netflix work" >
           <img class="image imagemagazine hidden" src="../images/hp-image-1.jpg" alt="examples of 1883 magazine work" >

           <!-- mobile images -->
           <img class="mob-image imageasos hidden-desk" src="../images/topshop-pdp-mob.jpg" alt="examples of asos work" >
           <img class="mob-image imagetopshop hidden-desk" src="../images/warehouse-lookbook-mob.jpg" alt="examples of topshop work" >
           <img class="mob-image imagemade hidden-desk" src="../images/topshop-pdp-mob.jpg" alt="examples of made work" >
           <img class="mob-image imagewarehouse hidden-desk" src="../images/warehouse-lookbook-mob.jpg" alt="examples of warehouse work" >
           <img class="mob-image imagerollacoaster hidden-desk" src="../images/topshop-pdp-mob.jpg" alt="examples of rollacoaster work" >
           <img class="mob-image imageselfridges hidden-desk" src="../images/warehouse-lookbook-mob.jpg" alt="examples of selfridges work" >
           <img class="mob-image imageharrods hidden-desk" src="../images/topshop-pdp-mob.jpg" alt="examples of harrods work" >
           <img class="mob-image imagenetflix hidden-desk" src="../images/warehouse-lookbook-mob.jpg" alt="examples of netflix work" >
           <img class="mob-image imagemagazine hidden-desk" src="../images/topshop-pdp-mob.jpg" alt="examples of 1883 magazine work" >
        </div>
      </div>
    </div>
    </div>
  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import Nav from '../components/Nav.vue'

  export default {
    data: function () {
      return {
        asosHover: false,
        topshopHover: false,
        madeHover: false,
        warehousepHover: false,
        rollacoasterHover: false,
        selfridgesHover: false,
        harrodsHover: false,
        netflixHover: false,
        magazineHover: false,
        isMobile: window.innerWidth <= 768 ? true : false
      }
    },
    components: {
      MainLayout, Nav
    },
    methods:{
      mobileScorll: function() {
          console.log('in mob scroll funct')

          var asosY = document.querySelector('#asos').getBoundingClientRect().top;
          var topshopY = document.querySelector('#topshop').getBoundingClientRect().top;
          var madeY = document.querySelector('#made').getBoundingClientRect().top;
          var warehouseY = document.querySelector('#warehouse').getBoundingClientRect().top;
          var rollacoasterY = document.querySelector('#rollacoaster').getBoundingClientRect().top;
          var selfridgesY = document.querySelector('#selfridges').getBoundingClientRect().top;
          var harrodsY = document.querySelector('#harrods').getBoundingClientRect().top;
          var netflixY = document.querySelector('#netflix').getBoundingClientRect().top;
          var magazineY = document.querySelector('#magazine').getBoundingClientRect().top;

          switch (true) {
            case asosY <= 150 && asosY >= -85:
                console.log('in')
                this.asosHover = true;
                this.topshopHover = false;
                this.madeHover = false;
              break;
            case topshopY <= 150 && topshopY >= -85:
                console.log('in2')
                this.asosHover = false;
                this.topshopHover = true;
                this.madeHover = false;
              break;
            case madeY <= 150 && madeY >= -85:
                console.log('in3')
                this.asosHover = false;
                this.topshopHover = false;
                this.madeHover = true;
              break;
            case warehouseY <= 150 && asosY >= -85:
              
              break;
            case rollacoasterY <= 150 && asosY >= -85:
              
              break;
            case selfridgesY <= 150 && asosY >= -85:
              
              break;
            case harrodsY <= 150 && asosY >= -85:

              break;
            case netflixY <= 150 && asosY >= -85:

              break;
            case magazineY <= 150 && asosY >= -85:

              break;
            default:
              this.asosHover = true;
              this.topshopHover = false;
              this.madeHover = false;
          }

        }
    }, 
    mounted: function() {
        var that = this;

        window.addEventListener('resize', function(e){         
            if (window.innerWidth <= 768) {
              that.isMobile = true;
            } else {
              that.isMobile = false;
            }
        });

        if (this.isMobile) {
          window.addEventListener('scroll', this.mobileScorll);
        }

    }
  }
</script>

<style scoped>

  .work {
    background-color: #fff;
    transition: background-color 1s ease;
  }

  h1 {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 40px;
    margin: 55px 0 200px;
    position: relative;
    z-index: 2;
  }

  ul {
    list-style: none;
  }

  li {
    font-family: 'Roboto-medium', sans-serif;
    margin: 0 0 200px 0;
    font-size: 30px;
    text-decoration: underline;
    cursor: url(../images/hover.png), pointer;
    opacity: 1;
    transition: opacity 1s ease;
    position: relative;
    z-index: 2;
  }

  li:last-of-type {
    margin: 0 0 400px 0;  
  }

  .image {
    position: absolute;
    opacity: 0;
    transition: opacity 1s ease;
    z-index: 1;
  }

  .mob-image {
    position: fixed;
    top: 50px;
    right: 0;
    z-index: 1;
    opacity: 0;
    transition: opacity .5s ease;
  }

 /* transitions */

  .asos .imageasos {
    opacity: 1;
  }

  .topshop .imagetopshop {
    opacity: 1;
  }

  .made .imagemade {
    opacity: 1;
  }

  .warehouse .imagewarehouse {
    opacity: 1;
  }

  .rollacoaster .imagerollacoaster {
    opacity: 1;
  }

  .selfridges .imageselfridges {
    opacity: 1;
  }

  .harrods .imageharrods {
    opacity: 1;
  }

  .netflix .imagenetflix {
    opacity: 1;
  }

  .magazine .imagemagazine {
    opacity: 1;
  }
  

  @media only screen and (max-width: 768px) {
    li {
      width: 100%;
    }

    .hidden {
      display: none;
    }
  }

  @media only screen and (min-width: 769px) {


    .hidden-desk {
      display: none;
    }

    h1 {
      margin: 100px 0 145px;
      font-size: 55px;
    }

    .work {
      height: calc(100vh - 90px);
      min-height: 500px;
      max-height: 800px;
    }

    ul {
      display: flex;
      flex-wrap: wrap;
    }

    li, li:last-of-type {
      margin: 0 20px 50px 0;
    }

    .image {
      top: 50%;
      transform: translateY(-50%);
      right: 10%;
    }

    .asos li:not(#asos) {
      opacity: 0;
    }

    .topshop li:not(#topshop) {
      opacity: 0;
    }

    .made li:not(#made) {
      opacity: 0;
    } 

    .warehouse li:not(#warehouse) {
      opacity: 0;
    }

    .rollacoaster li:not(#rollacoaster) {
      opacity: 0;
    }

    .selfridges li:not(#selfridges) {
      opacity: 0;
    }

    .harrods li:not(#harrods) {
      opacity: 0;
    }

    .netflix li:not(#netflix) {
      opacity: 0;
    } 

    .magazine li:not(#magazine) {
      opacity: 0;
    }

  }

</style>
