<template>
  <div class="full-image" v-bind:style="{ backgroundColor:  $props.bg }">
    <div class="container">
      <div class="row"> 
        <div class="col-1 hidden-sm"></div>
        <div class="col-10">

          <ul v-if="$props.images.length > 0">
            <li v-for="image in $props.images">
                <img v-bind:src="image.src" :alt="image.alt">
            </li>
          </ul>
          
        </div>
        <div class="col-1 hidden-sm"></div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {

    data: function () {
      return {
      }
    },
    props: {
      images: Array,
      bg: String
    },
    components: {
    },
    methods: {

    }
  }
</script>

<style scoped>

  .full-image {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content:center;
  }

  ul {
    display: grid;
    width: 100%;
    list-style: none;
    row-gap: 30px; 
    column-gap: 30px; 
    grid-template-columns: repeat(6, calc(16.66666666% - 25px));
  }

  li {
    height: 381px;
  }


  img {
    width: 100%;
    height: auto;
  }

  @media only screen and (min-width: 768px) {

    .full-image  {
      height: 100vh;
      min-height: 500px;
      max-height: 800px;
    }
  }



  @media only screen and (min-width: 1024px) {



  }

</style>
