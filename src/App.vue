<template lang="">
  
  <AppSearch @search="getMovies"/>
  <AppMain :movies="listaFilm" :series="listaSerieTv"/>

</template>
<script>


import AppSearch from './components/AppSearch.vue';
import AppMain from './components/AppMain.vue';
import axios from 'axios';

export default {
  name: 'app',
  components: {
    
    AppSearch,
    AppMain,
  },

  data() {
    return {
      listaFilm: [],
      listaSerieTv: [],
    }
  },

  methods:{
    getMovies(searchContent = '') {
      console.log(searchContent);

      axios.get('https://api.themoviedb.org/3/search/movie?api_key=3c92d587c03d41495b183d4688f2f790&query=' + searchContent)
        .then((response) => {
          console.log(response)
          this.listaFilm = response.data.results;
        })
        .catch(function(error) {
          console.log(error)
        });
    },

    getSeries(searchContent = '') {
      console.log(searchContent);

      axios.get('https://api.themoviedb.org/3/search/tv?api_key=3c92d587c03d41495b183d4688f2f790&query=' + searchContent)
        .then((response) => {
          console.log(response)
          this.listaSerieTv = response.data.results;

        })
        .catch(function(error) {
          console.log(error)
        });
    }

  },

  created() {
    this.getMovies('natale')
    this.getSeries('magia')
  },
  

  
 

  
  

  
}
</script>
<style lang="scss">
  @use './styles/general.scss' as *;
  
</style>

