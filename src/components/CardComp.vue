<template>
  <div>
    
      <h3>{{title}}</h3>
      <span>{{original_title}}</span>
      <span>{{original_language}}</span>
      <span>{{vote_average}}</span>
  </div>
</template>

<script>


export default {
  name: 'CardComp',
  
  props: {
    title: String,
    original_title: String,
    original_language: String,
    vote_average: Number,
  }
}
</script>

<style scoped lang="scss">
 /*Inserire style componente*/
 
</style>