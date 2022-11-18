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
  <div class="jt-container">
    <select @change="$emit('startSearch')" v-model="store.categoryToSearch" class="form-select">
      <option value="" selected>Select category</option>
      <option value="Breaking Bad">Breaking Bad</option>
      <option value="Better Call Saul">Better Call Saul</option>
    </select>

  </div>


  
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.jt-container{
  width: 70%;
  margin: 0 auto;
  select{
    width: 200px;
    margin-bottom: 20px;
  }

}


</style>