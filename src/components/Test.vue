


<script lang="ts">
import Vue from 'vue'
import draggable from 'vuedraggable';

export default Vue.extend({
  components: {
    draggable
  },
  data: function() {
    return{
      myArray: [
        {id: 1, name: 'couches', order: 1,},
        {id: 2, name: 'pot de confiture',order: 2},
        {id: 3, name: "coquilles d'oeufs",order: 3},
        {id: 4, name: 'boîtes de conserve', order: 4},
        {id: 5, name: 'marc de café',order: 5}
      ],
      mySecondArray: [{ id: 6, name: 'bravo'}]
    }
  },

})
</script>


<style>
  h2 {
    color: white;
  }
  #prout {
    background-color: darkturquoise;
    height: 400px;
  }
  #prout.drop_hover {
    box-shadow: 0 0 30px rgba(0,0,0,0.8) inset;
  }
  .colonne {
    color: black;
     border: solid 3px;
     font-size: 30px;
  }
  .div2 {
    background-color: red;
  }
  .div3 {
    background-color: orange;
  }
</style>

<!--// npm run serve -->