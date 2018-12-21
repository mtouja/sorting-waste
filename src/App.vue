<template>
  <div id="app">
    <Test />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Test from './components/Test.vue'

export default {
  name: 'app',
  components: {
    // HelloWorld,
    Test
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poiret+One');
#app {
  font-family: 'Poiret One', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #FFF;
  margin-top: 60px;

}
</style>




