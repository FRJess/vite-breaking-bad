<script>
import {store} from '../data/store';
import CharacterCard from './CharacterCard.vue';
import AppLoading from './AppLoading.vue';

export default {
  name: 'CharactersList',
  components: {
    CharacterCard,
    AppLoading,
  },
  data(){
    return{
      store
    }
  },
  computed:{
    getOutputCounter(){
      return store.charactersListData.length;
    }
  }
  
}
</script>

<template>

  <div class="main">

    <div class="col counter">
      <p class="p-2">
        Found {{ getOutputCounter }} characters
      </p>
    </div>

    <div
    v-if="store.isLoaded"
      class="content">
      <CharacterCard
      v-for="character in store.charactersListData"
      :key="character.char_id"
      :character="character"
      />
    </div>

    <div v-else class="loader">
      <AppLoading title="Characters loading..."/>
    </div>
      
  </div>
  
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.main{
  background-color: white;
  width: 70%;
  padding: 20px;
  margin: 0 auto;

  .counter{
    width: 92%;
    margin: 0 auto;
    background-color: darken($primary-color, 40%) ;
    font-family: $main-font;
    font-size: 0.8rem;
    font-weight: 600
  }

  .content {
    @include centerFlex('both');
    flex-wrap: wrap;
  }

  .loader{
    @include centerFlex('horizontal');
  }
}

</style>