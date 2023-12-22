<template lang="">
    <div class="container">
        <article v-for="movie in movies" class="text-center mt-3">
            <p>
                titolo: {{ movie.title}} <br> 
                titolo originale: {{ movie.original_title }} <br> 
                lingua originale: {{ movie.original_language }} <br>
                voto: {{ movie.vote_average }}
                <img :src="'http://image.tmdb.org/t/p/w500' + movie.backdrop_path" alt="">
                
            </p> 

        </article> 
        <article v-for="serie in series " class="mt-3">
            <p>

                titolo: {{ serie.name }} <br>
                titolo originale: {{ serie.original_name }} <br> 
                lingua originale: {{ serie.original_language }} <br>
                voto: {{ serie.vote_average }}
                <img :src=" 'http://image.tmdb.org/t/p/w500' + serie.backdrop_path " alt="">
              
            </p>

        </article>
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

   
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;


    
</style>