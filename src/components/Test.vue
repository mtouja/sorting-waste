
<template>
<draggable>
<b-container fluid class="bloc bv-example-row">
  <h1>Sais tu trier tes déchets?</h1>
  <b-row class="row no-gutter"> 
    <b-col class="c" cols="3">
      <template>
        <draggable v-model="myArray" :options="{group:'people'}" @start="drag=true" @end="drag=false" id="listItem">
        <div class="colonne" v-for="element in myArray" :key="element.id">
          <button>{{element.name}}</button>
        </div>
        </draggable> 
      </template> 
    </b-col>
    <b-col class="c" cols="9">
      <b-row class="row no-gutter">
        <b-col class="c" cols="4" offset="1">
          <template>
            <h3>Déchets organiques</h3>
            <draggable v-model="organique" :options="{group:'people'}" @start="drag=true" @end="drag=true" id="compost">
              <div class="colonne" v-for="element in organique" :key="element.id">
                <button>{{element.name}}</button>
              </div>
                <img class="waste" src='https://image.flaticon.com/icons/svg/1061/1061010.svg'/>
            </draggable>
          </template>  
        </b-col>
        <b-col class="c" cols="4" offset="1">
          <template>
            <h3>Plastiques</h3>
            <draggable v-model="plastique" :options="{group:'people'}" @start="drag=true" @end="drag=true" id="plastique">
              <div class="colonne" v-for="element in plastique" :key="element.id">
                <button>{{element.name}}</button>
              </div>
                <img class="waste" src='https://image.flaticon.com/icons/svg/1265/1265024.svg'/>
            </draggable>
          </template>
        </b-col>
      </b-row>
      <b-row>
        <b-col class="c" cols="4" offset="1">
          <template>
            <h3>Cartons</h3>
            <draggable v-model="carton" :options="{group:'people'}" @start="drag=true" @end="drag=true" id="carton">
              <div class="colonne" v-for="element in carton" :key="element.id">
                <button>{{element.name}}</button>
              </div>
                <img class="waste" src='https://image.flaticon.com/icons/svg/416/416186.svg'/>
            </draggable>
          </template>
        </b-col>
        <b-col class="c" cols="4" offset="1">
          <template>
            <h3>Poubelle ordinaire</h3>
            <draggable v-model="ordinaire" :options="{group:'people'}" @start="drag=true" @end="drag=true" id="ordinaire">
              <div class="colonne" v-for="element in ordinaire" :key="element.id">
                <button>{{element.name}}</button>
              </div>
                <img class="waste" src='https://image.flaticon.com/icons/svg/1341/1341939.svg'/>
            </draggable>
          </template>
        </b-col>
      </b-row>
    </b-col>
  </b-row>
  
</b-container>
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
        {id: 5, name: 'marc de café'},
        {id: 6, name: "bouteille de lait"},
        {id: 7, name: "boîtes d'oeufs"},
        {id: 8, name: 'bidon de lessive'},
        {id: 9, name: "coquilles pot de yaourt"},
        {id: 10, name: 'magazine'},
        {id: 11, name: 'papier gras'}
      ],
      organique: [
        ],
      plastique: [
        ],
      carton: [
      ],
      ordinaire: [
      ],
    }
  },
})
</script>

<style>
  html {
    background-color: #2a5b74;
  }
  .icon {
    width: 200px;
    margin-bottom: 30px;
  }
  .waste {
    width: 80px;
    margin-top: 20px;
  }
  #listItem {
    background-color: #2a5b74;
  }
  #compost{
    background-color: #00b896;
    height: 250px;
  }
  #plastique{
    background-color: #00b896;
    height: 250px;
  }
  #ordinaire {
    background-color: #00b896;
    height: 250px;
  }
  #carton {
    background-color: #00b896;
    height: 250px;
  }
  .col-3 {
    background-color: #2a5b74;
  }
  h3, h1 {
    background-color: #2a5b74;
    margin-bottom: 0 !important;
    padding-bottom: 30px;
    padding-top: 30px;
  }
  .colonne {
    font-size: 22px;
  }
  .row.no-gutters {
  margin-right: 0;
  margin-left: 0;
  background-color: #2a5b74!important;
  }
  .c {
    padding: 0 !important;
    background-color: #2a5b74 !important;
  }
  .container-fluid {
    padding: 0 !important;
  }
</style>