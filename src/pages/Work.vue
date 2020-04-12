<template>
  <main-layout>
    <Nav />
    <div class="work" :class="{asos: asosHover, topshop: topshopHover, made: madeHover, warehouse: warehousepHover, rollacoaster: rollacoasterHover, selfridges: selfridgesHover, harrods: harrodsHover, netflix: netflixHover, magazine: magazineHover}">
    <div v-if="isDesktop" class="follower hidden-sm"></div>
    <div class="container">
      <div class="row">
        <div class="col-1 hidden-sm"></div>
        <div class="col-4">
          <h1 data-aos="fade" data-aos-duration="1000">Work.</h1>
        </div>
        <div class="col-2 hidden-sm"></div>
        <div class="col-4">
          <h2 data-aos="fade" data-aos-duration="1000">Selected projects</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-1 hidden-sm"></div>
        <div class="col-10">
           <ul class="this" data-aos="fade" data-aos-duration="1000">
            <li id="asos"><span>01.</span><p class="underline" @mouseover="asosHover = true" @mouseleave="asosHover = false">ASOS.</p></li>
            <li id="topshop"><span>02.</span><p class="underline" @mouseover="topshopHover = true" @mouseleave="topshopHover = false">Topshop.</p></li>
            <li id="made"><span>03.</span><p class="underline" @mouseover="madeHover = true" @mouseleave="madeHover = false">Made.com.</p></li>
            <li id="warehouse"><span>04.</span><p class="underline" @mouseover="warehousepHover = true" @mouseleave="warehousepHover = false">Warehouse.</p></li>
            <li id="rollacoaster" ><span>05.</span><p class="underline" @mouseover="rollacoasterHover = true" @mouseleave="rollacoasterHover = false">Rollacoaster.</p></li>
            <li id="selfridges" ><span>06.</span><p class="underline" @mouseover="selfridgesHover = true" @mouseleave="selfridgesHover = false">Selfridges.</p></li>
            <li id="harrods"><span>07.</span><p class="underline" @mouseover="harrodsHover = true" @mouseleave="harrodsHover = false">Harrods.</p></li>
            <li id="netflix"><span>08.</span><p class="underline" @mouseover="netflixHover = true" @mouseleave="netflixHover = false">Netflix.</p></li>
            <li id="magazine"><span>09.</span><p class="underline" @mouseover="magazineHover = true" @mouseleave="magazineHover = false">1883 Magazine.</p></li>
          </ul> 

          <img class="mobile-image hidden-desk imageasos" src="../images/asos-colour.jpg" alt="example of asos work">
          <img class="mobile-image hidden-desk imagetopshop" src="../images/topshop-hero3.jpg" alt="example of asos work">
          <img class="mobile-image hidden-desk imagemade" src="../images/made-wishlist2.jpg" alt="example of asos work">
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
        isMobile: window.innerWidth <= 768 ? true : false,
        isDesktop: true,
      }
    },
    components: {
      MainLayout, Nav
    },
    methods:{
      mobileScorll: function() {
         
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
            case asosY <= 400 && asosY > 0:
                this.asosHover = true;
                this.topshopHover = false;
                this.madeHover = false;
              break;
            case topshopY <= 400 && topshopY > 0:
                
                this.asosHover = false;
                this.topshopHover = true;
                this.madeHover = false;
              break;
            case madeY <= 400 && madeY > 0:
                
                this.asosHover = false;
                this.topshopHover = false;
                this.madeHover = true;
              break;
            case warehouseY <= 400:
              
              break;
            case rollacoasterY <= 400:
              
              break;
            case selfridgesY <= 400:
              
              break;
            case harrodsY <= 400:

              break;
            case netflixY <= 400:

              break;
            case magazineY <= 400:

              break;
            default:
              this.asosHover = false;
              this.topshopHover = false;
              this.madeHover = false;
          }

        },
      checkDesktop: function() {
        var that = this;
        //check if desktop
        if( /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent) || window.innerWidth <= 768 ) {
          this.isDesktop = false;
          document.addEventListener('scroll', function(e) {
              that.mobileScorll();
          });
        } else {
          //if desktop add follower div to follow cursor
          this.isDesktop = true;
          document.addEventListener('mousemove', function(e) {
            document.querySelector('.follower').style.left = (e.pageX + 20) + "px";
            document.querySelector('.follower').style.top = ( e.pageY + 20) + "px";
          });
        }
      }
    }, 
    mounted: function() {
      var that = this;

      this.checkDesktop();
      window.addEventListener('resize', function(e) {
        that.checkDesktop();
      });

       //deal with animation issue
      setTimeout(function(){ 
        
        document.querySelector('h1').classList.add('aos-animate');
        document.querySelector('h2').classList.add('aos-animate');
        document.querySelector('.this').classList.add('aos-animate');
        
        }, 200);
    }
  }
</script>

<style scoped>

  .main {
    padding: 0;
  }

  .work {
    background-color: #fff;
    transition: background-color 1s ease;
    padding: 90px 0 0 0;
  }

  .container, .row {
    height: unset;
  }

  h1 {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 40px;
    margin: 55px 0 0;
    position: relative;
    z-index: 2;
  }

  h2 {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 16px;
    margin: 90px 0 200px;
  }

  ul {
    list-style: none;
    z-index: 2;
    position: relative;
  }

  li {
    font-family: 'Roboto-medium', sans-serif;
    margin: 0 0 200px 0;
    font-size: 30px;
    opacity: 1;
    transition: opacity 1s ease;
    position: relative;
    z-index: 2;
  }

  li p {
    font-family: 'Roboto-medium', sans-serif;
    font-size: 30px;
    display: inline;
  }

  li span {
    font-size: 15px;
    padding: 0 20px 0 0;
  }

  li:last-of-type {
    margin: 0 0 400px 0;  
  }

  .mobile-image {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 1;
    opacity: 0;
    transition: opacity ease .5s;
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


  .asos.work {
    background-color: #C8C1BB;
  }

  .topshop.work {
    background-color: #BADA55;
  }

  .made.work {
    background-color: #B000B5;
  }

  .warehouse.work {
    background-color: #C8C1BB;
  }

  .rollacoaster.work {
    background-color: #C8C1BB;
  }

  .selfridges.work {
    background-color: #C8C1BB;
  }

  .harrods.work {
    background-color: #C8C1BB;
  }

  .netflix.work {
    background-color: #C8C1BB;
  }

  .magazine.work {
    background-color: #C8C1BB;
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

      h1 {
        margin: 100px 0 90px;
        font-size: 55px;
      }

      h2 {
        margin: 0 0 90px;
      }

    .hidden-desk {
      display: none;
    }

    .follower {
      height: 198px;
      width: 442px;
      position: absolute;
      float: left;
      opacity: 0 ;
      transition: opacity 1s ease;
      background-size: contain;
      background-repeat: no-repeat;
    }


    ul {
      display: flex;
      flex-wrap: wrap;
    }

    li, li:last-of-type {
      margin: 0 0 80px 0;
      width: 50%;
      box-sizing: border-box;
    }

    li:nth-child(even) {
      padding: 0 0 0 12%;
    }

    .image {
      top: 50%;
      transform: translateY(-50%);
      right: 10%;
    }

    .underline {
      display: inline;
      position: relative;
      overflow: hidden;
    }
    .underline:after {
      content: "";
      position: absolute;
      z-index: -1;
      right: 0;
      width: 0;
      bottom: -5px;
      background: #000;
      height: 3px;
      transition-property: width;
      transition-duration: 0.3s;
      transition-timing-function: ease-out;
    }
    .underline:hover:after,
    .underline:focus:after,
    .underline:active:after {
      left: 0;
      right: auto;
      width: 100%;
    }

    .asos .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .topshop .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .made .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .warehouse .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .rollacoaster .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .selfridges .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .harrods .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .netflix .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

    .magazine .follower {
      opacity: 1;
      background-image: url('../images/asos-purchase.png');
    }

  }

    @media only screen and (min-width: 1024px) {

      h1 {
        margin: 100px 0 145px;
      }

      h2 {
        margin: 135px 0 0;
      }
    }

</style>
