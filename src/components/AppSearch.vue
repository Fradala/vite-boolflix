<template lang="">
    <section class="bg-dark">
        <div class="container">
            <div class="titolo-ricerca col-12">
                <div class="text-uppercase">
                <h1 class="fs-4 mt-3">
                        boolflix
                </h1>
                </div>
                <div>
                    <input type="text" v-model="searchedString" @keyup.enter="$emit('search', searchedString)">
                </div>
                
            </div>
            
        </div>
    </section>
</template>
<script>
export default {
    name: 'AppSearch',
    data() {
        return{
            searchedString: '',
        }
    }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.titolo-ricerca{
    
    display: flex;
    align-items: center;
    justify-content: space-between;

    h1{
        color: red;
    }
}
    
</style>