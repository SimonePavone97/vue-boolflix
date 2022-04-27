<template>
  <div>
    <HeaderComp @funzioneRicerca="metodoSearch" />

    <MainComp :arrayFilm="FilmsArray" :arraySerie="SeriesArray" />

  </div>
</template>

<script>
  import "bootstrap"
  import axios from 'axios';
  import HeaderComp from './components/HeaderComp.vue'
  import MainComp from './components/MainComp.vue'

  export default {
    name: 'App',
    components: {
      HeaderComp,
      MainComp
    },

    data() {
      return {
        api_key: 'e9b260822f54b240e9160b0ae763ca01',
        query: 'star',
        FilmsArray: [],
        SeriesArray: [],
        testoRicerca: ''
      }
    },
    created() {

      axios.get(`https://api.themoviedb.org/3/search/movie?api_key=${this.api_key}&query=star`)
        .then((res) => {

          console.log(res.data.results);

          this.FilmsArray = res.data.results
        }),

        axios.get(`https://api.themoviedb.org/3/search/tv?api_key=${this.api_key}&query=star`)
        .then((res) => {

          console.log(res.data.results);

          this.SeriesArray = res.data.results
        })

        .catch((error) => {
          console.log(error)
        })
    },
    methods: {
      metodoSearch(testo) {
        console.log(testo)
        this.testoRicerca = testo
        console.log(this.testoRicerca)
      }
    }

    }
</script>

<style lang="scss">
  @import "bootstrap/dist/css/bootstrap.min.css";
</style>