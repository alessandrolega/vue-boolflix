<template>
    <div class="card" style="width: 18rem;">
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



</style>