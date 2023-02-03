<template>
  <div class="home">
    <NavMenu/>
    <div class="col">
      <h1>Home</h1>
    </div>
  </div>
</template>

<script>
import NavMenu from '@/components/NavMenu.vue';
export default {
  name: 'HomeView',
  components: {
    NavMenu
  }
}
</script>

<style>
.home{
  height: 100vh;
  background: url('https://www.techhive.com/wp-content/uploads/2022/10/shutterstock_1962278488.jpg?quality=50&strip=all') #0f0d00ec no-repeat;
  background-size: cover;
  background-blend-mode: overlay;
}

.home .col{
  height: 90%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.home .col h1{
  color: #f2f2f2;
}
</style>
