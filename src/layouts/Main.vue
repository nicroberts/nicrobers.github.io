<template>
  <div class="main">
    <Nav />
    <slot></slot>
  </div>
</template>

<script>
  import VLink from '../components/VLink.vue'
  import Nav from '../components/Nav.vue'

  export default {
    components: {
      VLink, Nav
    }
  }
</script>

<style scss>

  html, body, p, h1, h2, h3, a, div, ul, li {
    margin: 0;
    padding: 0;
    font-family: 'Roboto', sans-serif;
  }

  .container {
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    height: 100%; 
  }

  .row {
    position: relative;
    width: 100%;
    height: 100%;
  }

  .row [class^="col"] {
    float: left;
    margin: 0 2%;
    min-height: 0.125rem;
  }

  .row::after {
    content: "";
    display: table;
    clear: both;
  }

  .hidden-sm {
    display: none;
  }

  .hidden-ms {
    display: inherit;
  }

  .col-1,
  .col-2,
  .col-3,
  .col-4,
  .col-5,
  .col-6,
  .col-7,
  .col-8,
  .col-9,
  .col-10,
  .col-11,
  .col-12 {
    width: 96%;
  }

  @media only screen and (min-width: 1024px) {

    .container {
      max-width: 1440px;
    }

    .col-1 { width: calc((96% / 12) - (2% * 11 / 12)); }
    .col-2 { width: calc((96% / 6) - (2% * 10 / 12)); }
    .col-3 { width: (96% / 4) - (2% * 9 / 12); }
    .col-4 { width: (96% / 3) - (2% * 8 / 12); }
    .col-5 { width: (96% / (12 / 5)) - (2% * 7 / 12); }
    .col-6 { width: calc((96% / 2) - (2% * 6 / 12)); }
    .col-7 { width: (96% / (12 / 7)) - (2% * 5 / 12); }
    .col-8 { width: (96% / (12 / 8)) - (2% * 4 / 12); }
    .col-9 { width: (96% / (12 / 9)) - (2% * 3 / 12); }
    .col-10 { width: calc(96% / (12 / 10) - (2% * 2 / 12)); }
    .col-11 { width: (96% / (12 / 11)) - (2% * 1 / 12); }
    .col-12 { width: 96%; }

    .hidden-sm {
      display: block;
    }

    .hidden-ms {
      display: none;
    }
  }



</style>
