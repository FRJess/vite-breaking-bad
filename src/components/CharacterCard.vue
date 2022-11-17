<script>
export default {
  name: 'CharacterCard',
  props:{
    character: Object
  }
}
</script>

<template>

  <div class="card col-2">
    <img :src="character.img" :alt="character.name">

    <div class="jt-card-body">
      <h5>{{character.name}}</h5>
      <p>{{character.category}}</p>
      <p>{{character.status}}</p>
    </div>

  </div>
  
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use "../styles/partials/mixins" as *;

.card{
  text-align: center;
  margin: 10px;
  background-color: $primary-color;
  border-radius: 0;
  padding-bottom: 20px;
  img{
    padding: 10px;
    height: 200px;
    @include image-position();
  }
  h5{
    text-transform: $text-upper;
    font-size: 0.8rem;
    font-weight: 700;
    margin-bottom: 20px;
  }
  p{
    color: $secondary-color;
    font-size: 0.8rem;
  }
}


</style>