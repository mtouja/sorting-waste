
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
            </draggable>
          </template>
            <template>
              <b-btn class="btn btn-warning chiffres" v-b-modal.modal1>Le saviez-vous ?</b-btn>
                <b-modal class="compost" id="modal1" title="20 Millions">
                  <p>C'est le nombre de tonnes d'émission de CO2 évités grâce au recyclage.</p>
                </b-modal>
            </template>
        </b-col>
        <b-col class="c" cols="4" offset="1">
          <template>
            <h3>Plastiques</h3>
            <draggable v-model="plastique" :options="{group:'people'}" @start="drag=true" @end="drag=true" id="plastique">
              <div class="colonne" v-for="element in plastique" :key="element.id">
                <button>{{element.name}}</button>
              </div>
            </draggable>
          </template>
            <div>
              <b-btn class="btn btn-warning chiffres" v-b-modal.modal1>Le saviez-vous ?</b-btn>
                <b-modal class="plastique" title="1 Million">
                  <p>C'est le nombre de bouteilles en plastique vendues par minute. Soit 480 milliards pour l'année 2016.</p>
                </b-modal>
            </div>
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
            </draggable>
          </template>
          <div>
              <b-btn class="btn btn-warning chiffres" v-b-modal.modal1>Le saviez-vous ?</b-btn>
                <b-modal class="compost" id="cartons" title="test">
                  <p>bleble</p>
                </b-modal>
            </div>
        </b-col>
        <b-col class="c" cols="4" offset="1">
          <template>
            <h3>Poubelle ordinaire</h3>
            <draggable v-model="ordinaire" :options="{group:'people'}" @start="drag=true" @end="drag=true" id="ordinaire">
              <div class="colonne" v-for="element in ordinaire" :key="element.id">
                <button>{{element.name}}</button>
              </div>
            </draggable>
          </template>
          <div>
              <b-btn class="btn btn-warning chiffres" v-b-modal.modal1>Le saviez-vous ?</b-btn>
                <b-modal class="compost" id="compost" title="20 Millions">
                  <p>ordinaire.</p>
                </b-modal>
            </div>
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
        {id: 1, name: 'couches', info:'i'},
        {id: 2, name: 'epluchures'},
        {id: 3, name: "coquilles d'oeufs"},
        {id: 4, name: 'boîtes de conserve'},
        {id: 5, name: 'marc de café'},
        {id: 6, name: "bouteille de lait"},
        {id: 7, name: "boîtes d'oeufs"},
        {id: 8, name: 'bidon de lessive',info:'i'},
        {id: 9, name: "coquilles pot de yaourt"},
        {id: 10, name: 'magazine', info:'i'},
        {id: 11, name: 'papier gras'},
        {id: 12, name: 'journaux'}
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
  .chiffres {
    margin-top: 10px;
    font-weight: bold;
    font-size: 30px;
    font-family: 'Cairo';
  }
  .modal-header {
    text-align: center !important;
    border-bottom: transparent !important;
  }
  .modal-footer {
    border-top: transparent !important;
  }
  .waste {
    width: 80px;
    margin-top: 20px;
  }
  #listItem {
    background-color: #2a5b74;
  }
  p {
    font-family: 'Poiret One';
    font-size: 22px;
  }
  #compost{
    background-color: #00b896;
    height: 250px;
    background-image: url('https://image.flaticon.com/icons/svg/1061/1061010.svg');
    background-repeat: no-repeat;
    background-size: 80px 80px;
    background-position-x: center;
    background-position-y: center;
  }
  #plastique{
    background-color: #00b896;
    height: 250px;
    background-image: url('https://image.flaticon.com/icons/svg/1265/1265024.svg');
    background-repeat: no-repeat;
    background-size: 80px 80px;
    background-position-x: center;
    background-position-y: center;
  }
  #ordinaire {
    background-color: #00b896;
    height: 250px;
    background-image: url('https://image.flaticon.com/icons/svg/1341/1341939.svg');
    background-repeat: no-repeat;
    background-size: 80px 80px;
    background-position-x: center;
    background-position-y: center;
  }
  .modal-title  {
    text-align: center !important;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #e8d93d;
  }
  #carton {
    background-color: #00b896;
    height: 250px;
    background-image: url('https://image.flaticon.com/icons/svg/416/416186.svg');
    background-repeat: no-repeat;
    background-size: 80px 80px;
    background-position-x: center;
    background-position-y: center;
  }
  .col-3 {
    background-color: #2a5b74;
  }
  h3, h1 {
    background-color: #2a5b74;
    margin-bottom: 0 !important;
    padding-top: 30px;
  }
  h1 {
    text-align: center;
    margin-top: 20px;
  }
  h3 {
    margin-bottom: 20px;
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
  .modal-body, .modal-header, .modal-footer {
    background-color:#2a5b74;
    font-family:'Cairo';
    font-size: 20px;

  }
</style>