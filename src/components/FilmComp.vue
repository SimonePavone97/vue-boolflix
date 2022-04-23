<template>
    <main>
        
    
    <CardComp
      v-for="( element, index ) in FilmsArray"
      :key="index"
      :title="element.title"
      :original_title="element.original_title"
      :original_language="element.original_language"
      :vote_average="element.vote_average"
    />

  
    </main>
</template>

<script>
    
    import axios from 'axios';
    import CardComp from '../components/CardComp.vue'
    

    export default {
        name: 'FilmComp',
        components: {
            CardComp
        },

        data() {
            return {
                
                FilmsArray: []
            }
        },
        created() {
           
            axios.get(
                    'https://api.themoviedb.org/3/search/movie?api_key=e9b260822f54b240e9160b0ae763ca01&query=ritorno+al+futuro'
                    )
                .then((res) => {
                    console.log(res.data.results);
                    this.FilmsArray = res.data.results
                })
                .catch((error) => {
                    console.log(error)
                })
        }
    }
</script>

<style scoped lang="scss">
    /*Inserire style componente*/
</style>