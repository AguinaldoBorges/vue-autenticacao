<template>
  <div class="login">
    <div class="col-md-4">
      <img alt="Vue logo" src="../assets/logo.png" id="logo">
      <h1>PatoFlix</h1>
    <LoginForm/>
    </div>
  </div>
</template>

<script>
import LoginForm from '@/components/LoginForm.vue';

export default {
  name: 'LoginView',
  components: {
    LoginForm
  },
  beforeMount() {
    if(localStorage.getItem('loged') === 'true'){
      console.log(localStorage.getItem('loged'))
      this.$router.push('/home')
    }
  }
}
</script>

<style>
.login{
  height: 100vh;
  background: url('https://external-preview.redd.it/B6MrrY-dyD1lnvvrb2BCISx1xQwGx-e7pjm-qeXwAkE.jpg?auto=webp&s=ade83a5a759042ffed5324e5172c9a59a27aaaa9') no-repeat;
  background-size: cover;
  background-color: #0f0f0f;
  background-blend-mode: overlay;
  display: flex;
  align-items: center;
  justify-content: center;
}

.login #logo{
height: 180px;
width: 180px;
margin-bottom: 15px;
}
.login h1{
  color: #ff0707;
  font-weight: 700;
  letter-spacing: 3px;
  }
</style>
