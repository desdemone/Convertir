<template>
  <Convertisseur/>
</template>

<script>
import Convertisseur from'./components/Convertisseur.vue'
export default {
  name: 'App',
  components: {
   Convertisseur

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
  margin-top: 60px;
}
body{
  background: no-repeat url('./assets/photo.jpg');
  background-size: cover;
}
</style>
