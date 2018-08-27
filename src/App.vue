<template>
  <div id="app">

    <img src="./assets/logo.png">
    
    <MyForm />
    
  </div>
</template>

<script>
import MyForm from './components/MyForm'

export default {
  name: 'App',
  components: {
    MyForm
  }
}
</script>

<style lang="sass">
*
  box-sizing: border-box
  margin: 0
  padding: 0
#app 
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  color: black
  img
    display: block
    margin: 0 auto 30px

</style>
