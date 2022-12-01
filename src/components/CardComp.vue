<template>
    <div class="card" style="width: 18rem;">
        <img :src="`http://image.tmdb.org/t/p/w342/${singleFilm.poster_path}`" class="card-img-top" alt="poster">
        <div class="card-body">
            <h5 class="card-title">{{singleFilm.title}}</h5>
            <ul>
                <li>{{singleFilm.original_title}}</li>
                <li>{{singleFilm.original_language}}</li>
                <li>{{singleFilm.vote_average}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'CardComp',
        props:{
            singleFilm: Object
        }
    }
</script>

<style lang="scss" scoped>

.card{
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

.card:hover img{
    display: none;

}

.card:hover .card-body{
    display: block;
}


</style>