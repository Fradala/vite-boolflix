<template lang="">
    <header class="container">
        <nav class="navbar">
            <form class="d-flex" role="search">
                <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
            </form>
            
        </nav>
        
    </header>
    
</template>
<script>

export default {
    name: 'AppHeader',
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    
</style>