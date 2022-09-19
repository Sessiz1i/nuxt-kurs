<template>
  <v-container>
    <div class="col-md-4 mx-auto" style="min-width: 550px">
      <div class="mb-3"><h1>Login</h1></div>
      <UserAuthForm buttonText="Login" :submitForm="loginUser" />
    </div>
  </v-container>
</template>

<script>
import UserAuthForm from '~/components/UserAuthForm'
export default {
  name: 'login',
  components:{
    UserAuthForm
  },
  methods:{
    loginUser(){
      alert('Butona bastın')
    }
  }
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  min-height: calc(100vh - 100px);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
