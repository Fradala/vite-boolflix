<template lang="">
    <div>
        <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">search new film</span>
            <input type="text" class="form-control" placeholder="New film" aria-label="New film" 
            aria-describedby="basic-addon1" @keyup.enter="$emit('search')" v-model="store.searchMovie">
        </div>
    </div>
</template>
<script>
import { store } from '../js/store';
export default {
    data() {
        return{
            store,
        }
    }
    
}
</script>
<style lang="scss">
    
</style>