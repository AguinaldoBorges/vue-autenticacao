<template>
  <div class="login-form container">
    <div class="row">
      <div class="col-12">
        <form>
          <div class="mb-3">
            <label for="user" class="form-label">Email</label>
            <input type="email" class="form-control" id="user" aria-describedby="userHelp" v-model="user">
            <div id="userHelp" class="form-text">Nunca compartilharemos seu e-mail com mais ninguém.</div>
          </div>
          <div class="mb-3">
            <label for="passorwd" class="form-label">Senha</label>
            <input type="password" class="form-control" id="passorwd" v-model="password">
          </div>

          <button type="button" class="btn mt-3" @click="autenticate(user, password)">Entrar</button>
        </form>
      </div>
      <div class="col-12 d-flex justify-content-center" v-if="error">
        <div class="alert alert-danger" role="alert">
          Email ou Senha invalidos. Tente novamente!
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'LoginForm',
  data() {
    return {
      user: '',
      password: '',
      error: false
    }
  },
  methods: {
    autenticate(user, password){
      if(user === 'admin' && password === 'admin'){
        localStorage.setItem('loged', true);
        console.log('Logado');
        this.$router.push('/home')
      } else{
        this.error = true;
        setTimeout(() => {
          this.error = false
        }, 5000);
      }
    }
  },

}
</script>

<style>
.login-form{
  background: #8a878728;
  padding: 20px;
  border-radius: 5px;
}

.login-form label{
  text-align: left;
  color: #ffffff;
  width: 100%;
}
.login-form input{
  text-align: center;
  background: #20030396;
  color: #dfe7ec;

}

.login-form #userHelp{
  color: #dfe7ec;
}

.login-form .btn{
  color: #dfe7ec;
  background: #FF0707;
}

.login-form .btn:hover{
  color: #dfe7ec;
  background: #ff0707c2;
}

.login-form .alert{
  position: absolute;
  bottom: -10px;

  animation: fadein 2s;
}

@keyframes fadein {
  from { opacity: 0; }
  to   { opacity: 1; }
}
</style>
