<template>
  <div id="app">
    <p>HELLO DEAR GUEST!</p>
    <router-link to="/catalog">Catalog</router-link>
    <v-main-wrapper />
  </div>
</template>

<script>
import vMainWrapper from './components/v-main-wrapper'


export default {
  name: 'App',
  components:{
    vMainWrapper
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: #FDF5E6;
  padding: 10px;
}
</style>
