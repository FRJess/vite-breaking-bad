<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppSearch from './components/AppSearch.vue';
import CharactersList from './components/CharactersList.vue';

export default {
  name: 'App',

  components:{
    AppHeader,
    AppSearch,
    CharactersList,
  }
  
}
</script>

<template>

<AppHeader title="Breaking Bad Api"/>
<AppSearch/>
<CharactersList/>
  
</template>

<style lang="scss">

@use './styles/general';

</style>