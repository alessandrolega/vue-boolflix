<template>
    <main>
        <FilmComp/>
        <SeriesComp/>
        
    </main>
</template>

<script>

import FilmComp from './FilmComp.vue'
import SeriesComp from './SeriesComp.vue'

    export default {
        name: 'MainComp',
        components: {
            FilmComp,
            SeriesComp
        }
        
    }
</script>

<style lang="scss" scoped>

</style>