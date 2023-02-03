<template>
  <router-view />
</template>

<script>
export default {
  name: 'App',
  beforeMount() {
    if (localStorage.getItem('loged') === 'false') {
      console.log(localStorage.getItem('loged'))
      this.$router.push('/')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #b94242;
}
</style>
