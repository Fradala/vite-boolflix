<template lang="">
    <div class="container">
        <article v-for="movie in movies" class="text-center">
            <p>
                titolo: {{ movie.title}} <br> 
                titolo originale: {{ movie.original_title }} <br> 
                lingua originale: {{ movie.original_language }} <br>
                voto: {{ movie.vote_average }}
            </p> 

        </article>
        <article v-for="serie in series ">
            <p>
                
                titolo: {{ serie.title }}
                titolo originale: {{ serie.original_title }} <br> 
                lingua originale: {{ serie.original_language }} <br>
                voto: {{ serie.vote_average }}

              
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