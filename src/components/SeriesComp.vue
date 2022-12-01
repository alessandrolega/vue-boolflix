<template>
    <div class="d-flex flex-direction-column flex-wrap row-cols-6">
        <SeriesCard v-for="(element, index) in seriesData"
        :key="index"
        :singleSerie="element"/>
    </div>
</template>

<script>

import SeriesCard from './SeriesCard.vue'

    export default {
        name: 'SeriesComp',
        props:{
            seriesData: Array

        },
        components: {
            SeriesCard
        }
    }
</script>

<style lang="scss" scoped>

</style>