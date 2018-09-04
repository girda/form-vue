<template>
  <form class="my-form">

    <div class="my-form__row">
      <div class="my-form__row-el">
        <VInput 
          class="my-form__el"
          type="text" 
          id="first-name" 
          for="first-name" 
          label="First name"
          v-model="firstName"
          @input="v => setFirstName(v)" />
          <div class="error" v-if="!$v.firstName.minLength">errors</div>
      </div>

      <div class="my-form__row-el">
        <VInput
          class="my-form__el"
          type="text" 
          id="last-name" 
          for="last-name" 
          label="Last name"
          v-model="lastName"
          @input="v => setLastName(v)" />
          <div class="error" v-if="!$v.lastName.minLength">errors</div>
        </div>
    </div>

    <div class="my-form__row">
      <VInput
        class="my-form__el my-form__el--longer"
        type="text" 
        id="company" 
        for="company" 
        label="Company name"
        labelDescr="(optional)"
        v-model="companyName"/>

      <VInput
        class="my-form__el my-form__el--shorter"
        type="text" 
        id="nip" 
        for="nip" 
        label="Nip"
        labelDescr="(optional)"
        v-model="nip"/>
    </div>

    <div class="my-form__row">
      <VInput 
        type="text" 
        id="address" 
        for="address" 
        label="Address"
        v-model="address"/>
    </div>

    <div class="my-form__row">
      <VInput
        class="my-form__el"
        type="text" 
        id="city" 
        for="city" 
        label="City"
        v-model="city"/>

      <VInput
        class="my-form__el"
        type="text" 
        id="zipCode" 
        for="zipCode" 
        label="Zip code"
        v-model="zipCode"/>
    </div>

    <div class="my-form__row">
      <VInput
        class="my-form__el"
        type="tel" 
        id="tel" 
        for="tel" 
        label="Phone number"
        v-model="phoneNumber"/>

      <VInput 
        class="my-form__el"
        type="email" 
        id="email" 
        for="email" 
        label="email"
        v-model="email"/>
    </div>

    <button type="submit">Save</button>

  </form>
</template>

<script>
import VInput from './VInput'
import { required, minLength, between } from 'vuelidate/lib/validators'

export default {
  name: 'MyForm',
  components: {
    VInput
  },

  data () {
    return {
      firstName: '',
      lastName: '',
      email: '',
      companyName: '',
      nip: '',
      address: '',
      city: '',
      zipCode: '',
      phoneNumber: ''
    }
  },

  validations: {
    firstName: {
      required,
      minLength: minLength(4)
    },
    lastName: {
      required,
      minLength: minLength(4)
    }
  },

  methods: {
    setFirstName(value) {
      this.firstName = value
    },
    setLastName(value) {
      this.lastName = value
    }
  }
}
</script>

<style lang="sass">

.my-form
  width: 580px
  margin: 0 auto
  &__row
    display: flex
    justify-content: space-between
    margin-bottom: 35px
    &:last-of-type
      margin-bottom: 20px
    &-el
      width: 48%  
  &__el
    max-width: 100%
    &--longer
      max-width: 64%
    &--shorter
      max-width: 32%
  button[type=submit]
    display: block
    padding: 20px 80px
    margin: 0 auto
    font-size: 14px
    color: #ffffff
    text-transform: uppercase
    border: none
    background-color: #f68236
</style>
