<template>
  <div class="falling-image" v-bind:style="{left: $props.left}">
  </div>
</template>

<script>

  export default {

    data: function () {
      return {
      }
    },
    props: {
      left: String,
      duration: String,
      delay: String
    },
    components: {
    },
    mounted: function() {
      var animate = "fall infinite linear " + this.$props.duration + " " + this.$props.delay;
      console.log(animate)
      this.$el.style.animation = animate
    }
  }
</script>

<style >
  .falling-image {
    height: 40px;
    width: 40px;
    position: absolute;
    top: -40px;
    left: 0;
    background-image: url("../images/bad.png");
    background-size: contain;
    z-index: -1;

  }
  
  @keyframes fall {
    from {top: 0;}
    to {top: 100%;}
  }
</style>
