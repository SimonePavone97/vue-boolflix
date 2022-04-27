<template>
  <div class="mt-5 container">
    <div class="row row-cols-5 g-5">
      <FilmsComp :arrayFilm2="arrayFilm"
      v-for="( element, index ) in arrayFilm"
      :key="index"
      :title="element.title"
      :original_title="element.original_title"
      :language="element.original_language"
      :vote="element.vote_average"
    />

    <SeriesComp :arraySerie2="arraySerie"
      v-for="( subelement, subindex ) in arraySerie"
      :key="'a'+ subindex"
      :name="subelement.name"
      :original_name="subelement.original_name"
      :language="subelement.original_language"
      :vote="subelement.vote_average"
    />
    </div>
    
  </div>
</template>

<script>

import FilmsComp from './partials/FilmsComp.vue'
import SeriesComp from './partials/SeriesComp.vue'


export default {
  name: 'MainComp',
  components:{
    FilmsComp,
    SeriesComp
  },
  props: {
    arrayFilm: Array,
    arraySerie: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
