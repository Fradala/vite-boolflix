<template lang="">
    <div class="container">
        <input type="text" v-model="searchedString" @keyup.enter="$emit('search', searchedString)">
    </div>
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
<style lang="">
    
</style>