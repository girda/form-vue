<template>
  <div class="v-input">

    <label 
      :for="id">
      {{label}}
    </label>

    <input 
      :type="type" 
      :id="id"
    />

  </div>
</template>

<script>
export default {
  name: 'VInput',
  props: ['type','id','label'],
  data () {
    return {

    }
  }
}
</script>

<style lang="sass">

</style>
