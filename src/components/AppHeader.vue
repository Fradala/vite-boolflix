<template lang="">
    <header class="container">
        <nav class="navbar">
            <form class="d-flex" role="search">
                <input class="form-control me-2" type="text" placeholder="Search" 
                aria-label="Search" v-model="store.searchMovie" @keyup.enter="$emit('search')">
            </form>
            
        </nav>
        
    </header>
    
</template>
<script>

export default {
    name: 'AppHeader',
    data() {
        return {
            store,
        };
    },
    
};
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    
</style>