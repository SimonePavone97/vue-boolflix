<template>
    <main>

    </main>
</template>

<script>
    //Importiamo axios
    import axios from 'axios';

    export default {
        //Cambiare il nome con quello del componente creato
        name: 'FilmComp',
        data() {
            return {
                //Creare un array dove salvare i data della chiamata axios
                //Modificare il nome a piacere
                FilmsArray: []
            }
        },
        created() {
            //Qui utiliziamo axios
            //Modificare il link con l'api che si vuole usare
            axios.get(
                    'https://api.themoviedb.org/3/search/movie?api_key=e9b260822f54b240e9160b0ae763ca01&query=Spiderman&language=it-IT'
                    )
                .then((res) => {
                    //Controllo delle informazioni che otteniamo alla chiamata
                    console.log(res.data.results);
                    //Modifica dell'array dove salveremo i dati
                    this.FilmsArray = res.data.results
                })
                //Salvataggio in console di possibili errori
                .catch((error) => {
                    console.log(error)
                })
        }
    }
</script>

<style scoped lang="scss">
    /*Inserire style componente*/
</style>