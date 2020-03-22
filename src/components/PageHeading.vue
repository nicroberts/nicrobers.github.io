<template>
  <div class="page-heading" v-bind:style="{ backgroundColor:  $props.bg }">
    <div class="container" >
      <div class="row">
          <div class="col-1 hidden-sm"></div>
          <div class="col-4">
            <h1>{{ $props.title }}</h1>
          </div>
          <div class="col-5" >
            <p v-if="$props.sub" class="sub">{{ $props.sub }}</p>
            <p v-if="$props.para" class="para">{{ $props.para }}</p>
            <ul class="list" v-if="$props.list">
              <li v-for="item in $props.list" >
                {{item}}
              </li>
            </ul>
            <ul class="list-two" v-if="$props.list && $props.listTwo">
              <li v-for="item in $props.listTwo" >
                {{item}}
              </li>
            </ul>
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
      sub: String,
      para: String,
      bg: String,
      list: Array,
      listTwo: Array
    },
    components: {
    },
    methods: {

    }
  }
</script>

<style scoped>

  .page-heading {
    width: 100%;
    padding: 55px 0 100px;
  }

  h1 {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 70px;
  }


  .sub {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 20px;
    float: left;
    width: 100%;
    margin: 65px 0 0 ;
  }

  .para {
    font-size: 12px;
    float:right;
    width: 100%;
    margin: 15px 0 0 ;
  }

  .list, .list-two  {
    list-style: none;
    width: 100%;
  }

  .list {
    margin: 65px 0 0 ;
  }

  .list li, .list-two li  {
    font-family: 'Roboto-bold', sans-serif;
    font-size: 20px;
  }



@media only screen and (min-width: 768px) {

  .page-heading {
    padding: 80px 0 100px;
  }

  h1 {
    margin: 0 0 2rem;
  }

  .sub, .list {
    width: 50%;
    margin: 0;
    float: left;
  }

  .para, .list-two {
    width: 40%;
    margin: 0;
    float: right;
  }
}

</style>
