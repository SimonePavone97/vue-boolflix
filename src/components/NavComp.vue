<template>
<header>
  <nav class="navbar navbar-light bg-light">
      <div class="container-fluid">
        <img class="img-fluid" src="../assets/Netflix-PNG-File.png" alt="">
        <form class="d-flex">
          <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success" type="submit">Search</button>
        </form>
      </div>
    </nav>
</header>
    
</template>

<script>
  //import axios from 'axios';
  export default {

    name: 'NavComp',
  }
</script>

<style scoped lang="scss">

img{
  height: 100px;
}

</style>