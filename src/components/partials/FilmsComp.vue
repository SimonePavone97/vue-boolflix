<template>
  <div class="col">
    <div class="bg-dark text-white center p-3 card"
      :style="{ backgroundImage: `url( https://image.tmdb.org/t/p/w342${poster_path})`}">
      <h2 class="text-white mb-5">Films</h2>
      <h5 class="card-title">Titolo: {{title}}</h5>
      <h6 class="card-title">Titolo Originale: {{original_title}}</h6>
      <div class="card-text d-flex align-items-center">
        <span>Lingua: </span>
        <span class="flag ms-2"
          :class="( language == 'en') ? 'flag-en' : ( language == 'it') ? 'flag-it' : 'flag-unknown' ">

        </span>
      </div>

      <span class="card-text">Voto: {{vote}}</span>
    </div>

  </div>
</template>

<script>
  export default {

    name: 'FilmsComp',
    props: {
      arrayFilm2: Array,
      poster_path: String,
      title: String,
      original_title: String,
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

  .card {
    min-height: 400px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;

    position: relative;
    background: linear-gradient(rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.45));
  }

  .center{
    background-position: center;
  }
</style>