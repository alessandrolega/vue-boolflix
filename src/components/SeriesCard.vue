<template>
    <div class="card" style="width: 18rem;">
        <img :src="`http://image.tmdb.org/t/p/w342/${singleSerie.poster_path}`" class="card-img-top" alt="poster">
        <div class="card-body">
            <h5 class="card-title">{{singleSerie.name}}</h5>
            <ul>
                <li>{{singleSerie.original_name}}</li>
                <li>{{singleSerie.original_language}}</li>
                <li>{{singleSerie.vote_average}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'SeriesCard',
        props:{
            singleSerie: Object
        }
    }
</script>

<style lang="scss" scoped>

.card-body{
    display: block;
    background-color: #141414;
    color: white;
}

</style>