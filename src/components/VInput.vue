<template>
  <div class="v-input">

    <label 
      :for="id">
      {{label}} <span>{{labelDescr}}</span>
    </label>

    <input 
      :type="type"
      :id="id"
      :value="value"
      @input="updateValue($event.target.value)"
    />
  </div>
</template>

<script>
export default {
  name: 'VInput',
  props: ['type', 'id', 'label', 'value','labelDescr'],
  data () {
    return {
     
    }
  },

  methods: {
    updateValue(val) {
      this.$emit('input', val)
    }
  }
}
</script>

<style lang="sass">

.v-input
  display: flex
  flex-direction: column
  width: 100%
  label
    font-size: 10px
    text-transform: uppercase
    margin-bottom: 14px
    span
      text-transform: lowercase
  input
    font-size: 12px
    line-height: 42px
    padding: 0 15px




</style>
