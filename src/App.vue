<template>
  <div>
    <NavComp />

    <FilmComp />
  </div>


</template>

<script>
  import 'bootstrap'
  import NavComp from './components/NavComp.vue'
  import FilmComp from './components/FilmComp.vue'

  export default {
    name: 'App',
    components: {
      NavComp,
      FilmComp
    }
  }
</script>

<style lang="scss">
  @import "bootstrap/dist/css/bootstrap.min.css";
</style>