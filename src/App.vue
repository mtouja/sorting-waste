<template>
  <div id="app">
   <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
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
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #121212;
  margin-top: 60px;
}
</style>


