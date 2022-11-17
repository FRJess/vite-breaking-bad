<script>
import {store} from '../data/store';
import CharacterCard from './CharacterCard.vue';

export default {
  name: 'CharactersList',
  components: {
    CharacterCard,
  },
  data(){
    return{
      store
    }
  }
  
}
</script>

<template>

<div class="main">
    <div
      class="content">
      <CharacterCard
      v-for="character in store.charactersListData"
      :key="character.char_id"
      :character="character"
      />
    </div>
    
  </div>
  
</template>

<style lang="scss" scoped>

// @use './styles/general' as *;
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.main{
  background-color: white;
  width: 60%;
  padding: 20px;
  margin: 0 auto;
  .content {
    @include centerFlex('wrap');
  }
}



</style>