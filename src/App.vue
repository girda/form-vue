<template>
  <div id="app">
    <img src="./assets/logo.png">
    <VInput/>
  </div>
</template>

<script>
import VInput from './components/VInput'
export default {
  name: 'App',
  components: {
    VInput
  }
}
</script>

<style lang="sass">
#app 
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: red
  margin-top: 60px

</style>
