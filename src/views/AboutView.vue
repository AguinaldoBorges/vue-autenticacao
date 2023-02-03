<template>
  <div class="about">
    <NavMenu />
    <div class="col">
      <h1>About</h1>
    </div>
  </div>
</template>
<script>
import NavMenu from '@/components/NavMenu.vue';
export default {
  name: 'aboutView',
  components: {
    NavMenu
  }
}
</script>

<style>
.about{
  height: 100vh;
  background: url('https://prod-cdn-thekrazycouponlady.imgix.net/wp-content/uploads/2022/03/friends-netflix-dreamstime-2022-1646171320-1646171320.jpg') #0f0d00ec no-repeat;
  background-size: cover;
  background-blend-mode: overlay;
}

.about .col{
  height: 90%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.about .col h1{
  color: #f2f2f2;
}
</style>