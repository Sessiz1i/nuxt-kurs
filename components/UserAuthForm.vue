<template>
  <v-form v-model="valid">
    <v-text-field
      v-model="userInfo.name"
      :rules="[required('name')]"
      v-if="hasName"
      label="Name"
    />

    <v-text-field
      v-model="userInfo.email"
      :rules="[required('email'),emailFormat()]"
      label="Email"
    />

    <v-text-field class="mb-3"
      v-model="userInfo.password"
      :type="showPassword ? 'text': 'password'"
      :append-icon="showPassword ? 'mdi-eye':'mdi-eye-off'"
      @click:append="showPassword = !showPassword"
      :rules="[required('password'),minLength('password',8)]"
      label="Password"
      counter="true"
    />

    <v-btn class="float-end" @click="submitForm(userInfo)" :disabled="!valid">
      {{ buttonText }}
    </v-btn>
  </v-form>
</template>

<script>
import validations from '~/utils/validations'

export default {
  name: 'UserAuthForm',
  props: ['submitForm', 'buttonText', 'hasName'],
  data () {
    return {
      valid: false,
      showPassword: false,
      userInfo: {
        email: '',
        password: ''
      },
      ...validations
    }
  }
}
</script>

<style scoped>

</style>
