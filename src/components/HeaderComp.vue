<template>
  <header class="d-flex flex-direction-row justify-content-between align-items-center">
    <div class="logo-cont">
      <img src="../assets/Netflix-Logo.wine.svg" alt="">
    </div>
    <div>
      <input type="text" placeholder="Cerca..."
      v-model="ricerca"
      @keyup="$emit('nomeEmit', ricerca)">
    </div>
    
    
  </header>
</template>

<script>
export default {
  name: 'HeaderComp',
  data(){
    return{
      ricerca: ''
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

header{
  height: 100px;
  background-color: #0B0B0B;
  padding: 20px;
}

.logo-cont > img{
  width: 20%;
}

</style>
