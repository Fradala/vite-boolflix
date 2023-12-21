<template lang="">
    <div>
        <article v-for="movie in movies">
            <p>
                titolo: {{ movie.title}} <br> 
                titolo originale: {{ movie.original_title }} <br> 
                lingua originale: {{ movie.original_language }} <br>
                voto: {{ movie.vote_average }}
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
        }

    },
}
</script>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    
</style>