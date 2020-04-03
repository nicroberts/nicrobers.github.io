<template>
  <main-layout>
    <Nav />
    <div class="work" :class="{asos: asosHover}">
    <div class="container">
      <div class="row">
        <div class="col-1 hidden-sm"></div>
        <div class="col-10">
          <h1>Work.</h1>
           <ul>
            <li class="asos" @mouseover="asosHover = true" @mouseleave="asosHover = false">ASOS.</li>
            <li class="topshop">Topshop.</li>
            <li class="made">Made.com.</li>
            <li class="warehouse">Warehouse.</li>
            <li class="rollacoaster">Rollacoaster.</li>
            <li class="selfridges">Selfridges.</li>
            <li class="harrods">Harrods.</li>
            <li class="netflix">Netflix.</li>
            <li class="1883">1883 Magazine.</li>
          </ul> 
           <img class="image hidden" src="../images/hp-image-1.jpg" alt="examples of work" >
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
        asosHover: false
      }
    },
    components: {
      MainLayout, Nav
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
    margin: 55px 0 100px;
  }

  ul {
    list-style: none;
  }

  li {
    font-family: 'Roboto-medium', sans-serif;
    margin: 0 0 80px 0;
    font-size: 30px;
    text-decoration: underline;
    cursor: url(../images/hover.png), pointer;
    opacity: 1;
    transition: opacity 1s ease;
  }

  .image {
    position: absolute;
    opacity: 0;
    transition: opacity 1s ease;
    z-index: 1;
  }

  .asos li:not(.asos) {
    opacity: 0;
  }

  .asos .image {
    opacity: 1;
  }

  .asos.work {
    background-color: #B7B6BB;
  }

  

  @media only screen and (max-width: 768px) {
    li {
      width: 100%;
    }

    .hidden {
      display: none;
    }
  }

  @media only screen and (min-width: 768px) {

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

    li {
      margin: 0 20px 50px 0;
    }

    .image {
      top: 50%;
      transform: translateY(-50%);
      right: 10%;
    }

  }

</style>
