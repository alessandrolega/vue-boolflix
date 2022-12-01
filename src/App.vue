<template>
  <div id="app">
    <HeaderComp @nomeEmit="search"/>
    <MainComp :propsMain="arrayFilms" :propsSeries="arraySeries"/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },
  data(){
    return{
      apiKey: '485654aa1a6a37718a70aede92f8e01c',
      arrayFilms: [],
      arraySeries: []
    }
  },
  methods: {
    search(valueSearch){
      axios.get(`https://api.themoviedb.org/3/search/movie?api_key=${this.apiKey}&query=${valueSearch}`)
      .then((response)=>{
        this.arrayFilms = response.data.results
      });

      axios.get(`https://api.themoviedb.org/3/search/tv?api_key=${this.apiKey}&query=${valueSearch}`)
      .then((response)=>{
        this.arraySeries = response.data.results
      });

    },
  }
}
</script>

<style lang="scss">


#app {
  background-color: #141414;
  height: 100%;


}
</style>
