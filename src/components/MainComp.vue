<template>
    <main id="app">
        <div class="px-5">
            <h3 class="p-4 text-white">FILM</h3>
            <FilmComp :filmsData="propsMain"/>
            <div>
                <h3 class="p-4 text-white">SERIE TV</h3>
                <SeriesComp :seriesData="propsSeries"/>
            </div>
            
        </div>
        
        
    </main>
</template>

<script>

import FilmComp from './FilmComp.vue'
import SeriesComp from './SeriesComp.vue'

    export default {
        name: 'MainComp',
        props: {
            propsMain: Array,
            propsSeries: Array
        },
        components:{
            FilmComp,
            SeriesComp
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