<template>
  <div class="home">
    <img src="../assets/icon.png" class="icon" alt="">
    <h1>Bienvenido a facturatron</h1>
    <div v-if="!loggedIn">
      Para usar la app necesitas
      <router-link to="/login">
      <span>Acceder</span> 
      </router-link>
      o
      <router-link to="/register">
      <span>Registrate</span> 
      </router-link>
    </div>
  </div>
</template>

<script>
import { authComputed } from '../vuex/helpers'
export default {
  computed: {
    ...authComputed
  }
}
</script>
<style scoped>
  img{
    position: relative;
    top: -50px;
  }

  span{
    color: orangered
  }
</style>

