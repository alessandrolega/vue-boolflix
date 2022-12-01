<template>
    <div class="card" style="width: 18rem;">
        <img :src="`http://image.tmdb.org/t/p/w342/${singleSerie.poster_path}`" class="card-img-top" alt="poster">
        <div class="card-body">
            <h5 class="card-title">{{singleSerie.name}}</h5>
            <ul>
                <li>{{singleSerie.original_name}}</li>
                <li><img class="flag" :src=" `https://www.countryflagicons.com/SHINY/64/${ (singleSerie.original_language == 'en') ? 'GB' : ((singleSerie.original_language == 'ja') ? 'JP' : singleSerie.original_language.toUpperCase())}.png`"></li>
                <li>{{singleSerie.vote_average}}</li>
                <li>{{singleSerie.overview}}</li>
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

.flag{
    width: 30px;
}

.card{
    background-color: #141414;
}

.card-body{
    display: block;
    background-color: #141414;
    color: white;
}

.card > img{
    display: block;
}

.card-body{
    display: none;
    color: white;
}

.card:hover > img{
    display: none;

}

.card:hover .card-body{
    display: block;
}

</style>