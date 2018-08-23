<template>
  <div id="app">
    <img src="./assets/logo.png">
    <VInput 
      type="email" 
      id="email" 
      for="email" 
      label="email"
      v-model="email"/>
  </div>
</template>

<script>
import VInput from './components/VInput'
export default {
  name: 'App',
  components: {
    VInput
  },

  data () {
    return {
      email: ''
    }
  }
}
</script>

<style lang="sass">
#app 
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: black
  margin-top: 60px

</style>
