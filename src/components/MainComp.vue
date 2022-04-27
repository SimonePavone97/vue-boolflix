<template>
  <div>
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
      :title="subelement.name"
      :original_title="subelement.original_name"
      :language="subelement.original_language"
      :vote="subelement.vote_average"
    />
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
