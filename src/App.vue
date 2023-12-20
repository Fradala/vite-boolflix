<template lang="">
  <AppHeader />
  <AppSearch @search="newSearch"/>
  <AppMain/>

</template>
<script>
import axios from 'axios';
import { store } from './js/store';
import AppHeader from './components/AppHeader.vue';
import AppSearch from './components/AppSearch.vue';
import AppMain from './components/AppMain.vue';


export default {
  name: 'app',
  data() {
    return {
      store,
    }

  },
  components: {
    AppHeader,
    AppSearch,
    AppMain,
  },

  methods:{
    newSearch() {
      this.getCharactesr('https://api.themoviedb.org/3/search/movie?api_key=3c92d587c03d41495b183d4688f2f790&query=' + this.store.searchMovie);
    },

    getCharactesr(url = 'https://api.themoviedb.org/3/search') {
      axios.get(url)
        .then((response) => {
          console.log(response.data);
        })
        .catch(function (error) {
          console.log(error);
        });

    },

  },

  
}
</script>
<style lang="scss">
  @use './styles/general.scss' as *;
  
</style>

