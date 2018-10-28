<template>
  <div id="wrapper">
    <h1 align="center"> Beheer </h1>
    <Beheer></Beheer>
  </div>
</template>

<script>
import Beheer from './components/Beheer'

export default {
  name: 'App',
  components: {
    Beheer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#wrapper{
  width: 1200px;
  margin: auto;
  padding: auto;
  overflow: auto;
}
</style>
