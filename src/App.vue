<template lang="">
  <AppHeader/>
  <AppMain/>

</template>
<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'app',
  components: {
    AppHeader,
    AppMain,
  }
  
}
</script>
<style lang="scss">
  @use './styles/general.scss' as *;
  
</style>

