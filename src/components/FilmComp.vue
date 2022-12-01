<template>
    <div class="scrollmenu">
        <div class=" d-flex flex-direction-row row-cols-6">
        <CardComp v-for="(element, index) in filmsData"
        :key="index"
        :singleFilm="element"/>
    </div>
 
    </div>
   
</template>

<script>

import CardComp from './CardComp.vue'


    export default {
        name: 'FilmComp',
        props:{
            filmsData: Array
        },
        components: {
            CardComp
        },
        mounted(){
            

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