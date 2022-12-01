<template>
    <div class="card" style="width: 18rem;">
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

</style>