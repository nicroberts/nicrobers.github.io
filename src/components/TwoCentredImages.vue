<template>
  <div class="two-centered-images" >
    
    <div class="image-container" v-bind:style="{ backgroundColor:  $props.bg }" :class="{ bottom:  $props.bottomLeft }">
      <img :src="$props.images[0].src" :alt="$props.images[0].alt" data-aos="fade-up">
    </div>

    <div class="image-container" v-bind:style="{ backgroundColor:  $props.bg }" :class="{ bottom:  $props.bottomRight }">
      <img :src="$props.images[1].src" :alt="$props.images[1].alt" data-aos="fade-up">
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
      bottomLeft: Boolean,
      bottomRight: Boolean,
      bg: String
    },
    components: {
    },
    methods: {

    }
  }
</script>

<style scoped>

  .two-centered-images {
    width: 100%;
  }

  .image-container {
    width: 100%;
    height: 375px;
    background-position: center;
    background-size: cover;
    float: left;
    display:flex;
    justify-content: center;
    align-items: center;
  }

  img {
    max-height: 75%;
    max-width: 90%;
  }

  @media only screen and (min-width: 768px) {


    .image-container {
      width: 50%;
      height: 100%;
    }

    .image-container.bottom {
      align-items: flex-end;
    }

    .two-centered-images {
      height: 100vh;
      min-height: 500px;
      max-height: 800px;
    }

  }

  @media only screen and (min-width: 1024px) {
  }

</style>
