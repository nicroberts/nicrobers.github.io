<template>
  <div class="image-copy" :class="{ right:  $props.right }" v-bind:style="{ backgroundColor:  $props.bg }">

    <div class="image" v-bind:style="{ backgroundImage: 'url(' + $props.image + ')' }"></div>
    
    <div class="text-container">
      <h2 v-if="$props.head" class="header">{{ $props.head }}</h2>
      <p v-if="$props.text" class="text">{{ $props.text }}</p>
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
      right: Boolean,
      image: String,
      text: String,
      head: String,
      bg: String
    },
    components: {
    },
    methods: {

    }
  }
</script>

<style scoped>

  .image-copy {
    width: 100%;
  }

  .image {
    width: 100%;
    height: 375px;
    background-position: center;
    background-size: cover;
    float: left;
  }

  .text-container {
    float: right;
    box-sizing: border-box;
    margin: 0 6%;
  }

  .text {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 28px;
    margin: 40px 0 60px;
  }

  .header {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 14px;
    margin: 60px 0 0;
  }

  @media only screen and (min-width: 768px) {

    .image {
      width: 50%;
      height: 100%;
    }

    .image-copy {
      height: 100vh;
      min-height: 500px;
      max-height: 800px;
    }

    .text-container {
      margin: 0 10%;
      width: 30%;
      display: flex; 
     flex-direction: column; 
     justify-content: center;
      height: 100%;
    }

    .header {
      margin: 0 0 40px;
    }

    .text {
      margin: 0;
    }

    .image-copy.right {
      display: flex;
    }

    .right .image {
      order: 2;
    }
  }

  @media only screen and (min-width: 1024px) {

    .text {
      font-size: 35px;
    }

  }

</style>
