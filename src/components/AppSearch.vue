<script>
import {store} from '../data/store'

export default {
  name: 'AppSearch',
  data(){
    return{
      store
    }
  }
  
}
</script>

<template>
  <div class="container">
    <div class="col-2 py-3">
      <select @change="$emit('startSearch')" v-model="store.categoryToSearch" class="form-select">
        <option value="" selected>Select category</option>
        <option value="Breaking Bad">Breaking Bad</option>
        <option value="Better Call Saul">Better Call Saul</option>
      </select>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

// p{
//   font-family: $main-font;
//   color: $-color;
//   background-color: white;
// }

</style>