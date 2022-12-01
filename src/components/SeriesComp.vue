<template>
    <div class="scrollmenu">
        <div class="d-flex flex-direction-row row-cols-6">
        <SeriesCard v-for="(element, index) in seriesData"
        :key="index"
        :singleSerie="element"/>
    </div>
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

div.scrollmenu {
  background-color: #333;
  overflow: auto;
  white-space: nowrap;
}

</style>