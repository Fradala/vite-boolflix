<template lang="">
  <AppHeader @search="searchFilm"/>
  <AppMain/>

</template>
<script>

import AppHeader from './components/AppHeader.vue';
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
    AppMain,
  },

  methods:{
    searchFilm(){

    },
  }
  
}
</script>
<style lang="scss">
  @use './styles/general.scss' as *;
  
</style>

