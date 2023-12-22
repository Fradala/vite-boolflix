<template lang="">
    <div class="container">
        <div class="row">

        

            <h1 class="text-uppercase fs-3 mt-3 mb-3 text-center">
                movies
            </h1>
            <article v-for="movie in movies" class="mt-3">
                <div>
                    <img :src="'http://image.tmdb.org/t/p/w342' + movie.poster_path" alt="immagine del film">
                

            
                    <p class="">
                        titolo: {{ movie.title}} <br> 
                        titolo originale: {{ movie.original_title }} <br> 
                        lingua originale: {{ movie.original_language }} <br>
                        voto: {{ movie.vote_average }}   
                    </p> 
                </div>

            </article> 


            <h1 class="text-uppercase fs-3 mt-3 mb-3 text-center">
                Tv series
            </h1>
            <article v-for="serie in series " class="mt-3">
            


                <p>

                    titolo: {{ serie.name }} <br>   
                    titolo originale: {{ serie.original_name }} <br> 
                    lingua originale: {{ serie.original_language }} <br>
                    voto:  {{ arrotondaPerEccesso (serie.vote_average) }}
                    <img :src=" 'http://image.tmdb.org/t/p/w342' + serie.poster_path " alt="immagine della serie">
                
                </p>

            </article>
        </div>
    </div>
</template>
<script>
export default {
    name: 'AppMovie',

    props: {
        movies: {
            type: Array,
            required: true,
        },

        series:{
            type: Array,
            required: true,
        }

    

    },
    arrotondaPerEccesso(numero) {
        const risultato = Math.cell(numero / 5) * 5;
        return risultato;
    }

   
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


article{
    //width: calc((100% / 5) - 20px);


    img{
    width: 200px;
    height: 300px;

   

    }
}



    
</style>