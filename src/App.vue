<template lang="">
  <AppHeader />
  <AppSearch @search="newSearch"/>
  <AppMain/>

</template>
<script>
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
      console.log(this.store.searchMovie);
    },

  }
  
}
</script>
<style lang="scss">
  @use './styles/general.scss' as *;
  
</style>

