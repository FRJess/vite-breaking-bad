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
    <p class="hover">{{ character.nickname }}</p>

    <div class="jt-card-body">
      <h5>{{ character.name }}</h5>
      <p>{{ character.category }}</p>
      <p>{{ character.status }}</p>
    </div>

  </div>
  
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use "../styles/partials/mixins" as *;

.card{
  text-align: center;
  height: 300px;
  margin: 10px;
  background-color: $primary-color;
  border-radius: 0;
  padding-bottom: 20px;
  position: relative;
  img{
    padding: 10px;
    height: 180px;
    @include image-position();
  }
  .hover {
    @include text-center();
    color: white;
    opacity: 0;
    transition: 0.4s all;
    font-weight: 700;
    font-size: 0.6rem;
  }
  &:hover p {
    opacity: 1.4;
  }
  &:hover img {
    filter: brightness(0.4);
  }
  h5{
    text-transform: $text-upper;
    font-size: 0.7rem;
    font-weight: 700;
    margin-bottom: 20px;
    padding-top: 10px
  }
  p{
    color: $secondary-color;
    font-size: 0.8rem;
    margin: 0;
  }
}


</style>