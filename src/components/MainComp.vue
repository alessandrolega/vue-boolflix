<template>
    <main id="app">
        <div class="px-5">
            <h3 class="p-4 text-white">FILM</h3>
            <FilmComp :filmsData="propsMain"/>
        </div>
        
        
    </main>
</template>

<script>

import FilmComp from './FilmComp.vue'
// import SeriesComp from './SeriesComp.vue'

    export default {
        name: 'MainComp',
        props: {
            propsMain: Array
        },
        components:{
            FilmComp
        },
        methods: {

        }
        
    }
</script>

<style lang="scss" scoped>

main{
    background-color: #141414
}





</style>