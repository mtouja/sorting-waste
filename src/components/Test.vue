<template>
  <draggable v-model="myArray" :options="{group:'people'}" @start="drag=true" @end="drag=false" id="prout">
    <div class="colonne" v-for="element in myArray" :key="element.id">{{element.name}}</div>
    <div class="div2" style="height: 100px"></div>
    <div class="div3" style="height: 100px"></div>
  </draggable>
</template>

<script lang="ts">
import Vue from 'vue'
import draggable from 'vuedraggable'

export default Vue.extend({
  components: {
    draggable
  },
  data: function() {
    return{
      myArray: [
        {id: 1, name: 'couches'},
        {id: 2, name: 'pot de confiture'},
        {id: 3, name: "coquilles d'oeufs"},
        {id: 4, name: 'boîtes de conserve'},
        {id: 5, name: 'marc de café'}
      ]
    }
  }
})
</script>


<style>
  .juma {
    background-color: aqua;
  }
  h2 {
    color: white;
  }
  #prout {
    background-color: darkturquoise;
  }
  #prout.drop_hover {
    box-shadow: 0 0 30px rgba(0,0,0,0.8) inset;
  }
  .colonne {
    color: yellow;
  }
  .div2 {
    background-color: red;
  }
  .div3 {
    background-color: orange;
  }
</style>

<!--// npm run serve -->