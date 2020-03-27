<template>
  <div class="next-project" v-bind:style="{ backgroundColor:  $props.bg }">
    <div class="container" >
      <div class="row">
          <div class="col-1 hidden-sm"></div>
          <div class="col-4">
            <p v-if="$props.sub" class="sub">{{ $props.sub }}</p>
            <h1>{{ $props.title }}</h1>
          </div>
          <div class="col-2 hidden-sm"></div>
          <div class="col-3 flex" >
            <p v-if="$props.categories" class="categories">{{ $props.categories }}</p>
          </div>
          <div class="col-1 flex">

            <v-link href="/asos">
              <svg class="arrow" width="48px" height="34px" viewBox="0 0 48 34" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <g id="Symbols" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" stroke-linecap="square">
                    <g id="Desktop_Next_Project" transform="translate(-1210.000000, -180.000000)" stroke="#2D2D2D" stroke-width="2">
                        <g id="Group-2" transform="translate(1234.000000, 196.500000) rotate(-135.000000) translate(-1234.000000, -196.500000) translate(1217.000000, 180.000000)">
                            <path d="M22.2469517,32.5667568 L1.24695167,32.5667568" id="Line-2"></path>
                            <path d="M1.14034996,10.7530483 L1.14034996,31.7530483" id="Line-2"></path>
                            <path d="M32.9946474,0.708080802 L2.25735931,31.4452928" id="Line-2"></path>
                        </g>
                    </g>
                </g>
              </svg>
            </v-link>

          </div>
        </div>
    </div>
  </div>
</template>

<script>
  import VLink from '../components/VLink.vue'

  export default {

    data: function () {
      return {
      }
    },
    props: {
      title: String,
      categories: String,
      sub: String,
      bg: String,
    },
    components: {
      VLink
    },
    methods: {

    }
  }
</script>

<style scoped>

  .next-project {
    width: 100%;
    padding: 55px 0 100px;
  }

  h1 {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 40px;
    margin: 0 0 20px 0;
  }

  .categories {
    font-size: 15px;
    text-transform: uppercase;
    margin: 0 0 45px 0;
  }

  .sub {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 15px;
    margin: 55px 0 75px 0;
  }

  .arrow {
    height: 33px;
    width: 33px;
  }

  a {
    padding: 0;
  }


@media only screen and (min-width: 768px) {

  .next-project {
    padding: 80px 0 100px;
  }

  .sub {
    margin: 0 0 60px;
  }

  h1 {
    font-size: 55px;
  }


}

@media only screen and (min-width: 1024px) {

    h1 {
    margin: 0;
  }


  .categories, .arrow {
    margin: 0;
  }

  .flex {
    height: 136px;
    display: flex;
    justify-content: center;
    align-items: flex-end;
  }

}

</style>
