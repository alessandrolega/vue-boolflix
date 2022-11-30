<template>
  <header class="d-flex flex-direction-row justify-content-between align-items-center">
    <div class="logo-cont">
      <img src="../assets/Netflix-Logo.wine.svg" alt="">
    </div>
    <div>
      <input type="text" placeholder="Cerca..."
      v-model="ricercaFilm"
      @keyup="$emit('nomeEmit', ricercaFilm)">
    </div>
    
    
  </header>
</template>

<script>
export default {
  name: 'HeaderComp',
  data(){
    return{
      ricercaFilm: ''
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

header{
  height: 10%;
  background-color: #0B0B0B;
  padding: 20px;
}

.logo-cont > img{
  width: 20%;
}

</style>
