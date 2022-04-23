<template>
  <div>
    <NavComp />
  <div>
    <FilmComp />
    <CardComp/>
  </div>
    
  </div>


</template>

<script>
  import 'bootstrap'
  import NavComp from './components/NavComp.vue'
  import FilmComp from './components/FilmComp.vue'
  import CardComp from './components/CardComp.vue'

  export default {
    name: 'App',
    components: {
      NavComp,
      FilmComp,
      CardComp
    }
  }
</script>

<style lang="scss">
  @import "bootstrap/dist/css/bootstrap.min.css";
</style>