<template>
  <div>
    <h3 class="">{{name}}</h3>
    <h4 class="">{{original_name}}</h4>
    <span class="">{{language}}</span>
    <span class="">{{vote}}</span>
  </div>
</template>

<script>


  export default {
    
    name: 'SeriesComp',
    props: {
      arraySeries2: Array,
      name: String,
      original_name: String,
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