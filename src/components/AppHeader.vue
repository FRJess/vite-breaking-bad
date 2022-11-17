<script>
export default {
  name: 'AppHeader',
  props:{
    title: String,
  }
  
}
</script>

<template>

  <div class="jt-container d-flex inline">
    <img src="../assets/img/Breaking_Bad_logo.png" alt="logo breaking bad">
    <h1>{{title}}</h1>
  </div>
  
</template>

<style lang="scss" scoped>

// @use './styles/general' as *;
// @use '../styles/partials/variables' as *;
.jt-container{
  margin: 10px;
  h1{
    margin-left: 2px
  }
  img{
    height: 40px;
  }
}

</style>