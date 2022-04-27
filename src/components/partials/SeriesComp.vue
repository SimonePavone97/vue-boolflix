<template>
  <div class="col">
    <div class="bg-dark text-white p-3 card">
      <h2 class="text-white mb-5">Series</h2>
      <h5 class="card-title"> {{name}}</h5>
      <h6 class="card-title">{{original_name}}</h6>
      <div class="card-text d-flex align-items-center">
        <span>Lingua: </span>
        <span class="flag ms-2"
          :class="( language == 'en') ? 'flag-en' : ( language == 'it') ? 'flag-it' : 'flag-unknown' ">

        </span>
      </div>

      <span class="">{{vote}}</span>
    </div>

  </div>
</template>

<script>
  export default {

    name: 'SeriesComp',
    props: {
      arraySerie2: Array,
      name: String,
      original_name: String,
      language: String,
      vote: Number,
    }

  }
</script>

<style scoped lang="scss">
  .flag {
    background-size: contain;
    height: 24px;
    width: 24px;
    background-repeat: no-repeat;
    display: inline-block;
  }

  .flag-it {
    background-image: url('../../assets/icons8-italy-48.png');
  }

  .flag-en {
    background-image: url('../../assets/icons8-great-britain-48.png');
  }

  .flag-unknown {
    background-image: url('../../assets/Ellipse 1.png');
  }
</style>