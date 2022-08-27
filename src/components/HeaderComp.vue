<template>
  <header>
    <nav class="navbar navbar-danger bg-danger">
      <div class="container-fluid">
        <img class="img-fluid" src="../assets/Netflix-PNG-File.png" alt="">
        <form class="d-flex">
          <input v-model="searchText" 
          class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button 
          @click.prevent="$emit( 'funzioneRicerca', searchText )" 
          class="btn btn-outline-success"
            type="submit">Search</button>
        </form>
      </div>
    </nav>
  </header>
</template>

<script>
  export default {
    name: 'HeaderComp',
    data() {
      return {
        searchText: '',
      }
      
    }
    
  }
</script>


<style scoped lang="scss">
  img {
    width: 60px;
    height: 60px;
  }
</style>