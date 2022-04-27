<template>
  <div>
    <h3 class="">{{title}}</h3>
    <h4 class="">{{original_title}}</h4>
    <span class="">{{language}}</span>
    <span class="">{{vote}}</span>
  </div>
</template>

<script>
  export default {
    
    name: 'FilmsComp',
    props: {
      arrayFilm2: Array,
      title: String,
      original_title: String,
      language: String,
      vote: Number,
    }

  }
</script>

<style scoped lang="scss">
  /*Inserire style componente*/
  /*.divider{
   width: 30%;
   height: 1px;
   background-color: #1a1a1a;
   margin: 0 auto;
 }*/
</style>