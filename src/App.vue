<template>
  <Convertisseur />
</template>

<script>
import Convertisseur from "./components/Convertisseur.vue";
export default {
  name: "App",
  components: {
    Convertisseur,
  },
};
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
body {
  background: no-repeat url("./assets/photo.jpg");
  background-size: cover;
  background-position: left;
  background-attachment: fixed;
  min-height: 100%;
}
@media (max-width: 1000px) {
  h1 {
    font-size: 2.5em !important;
    width: 100%;
    margin-left: 400px !important;
  }
  input {
    width: 30% !important;
  }
}
@media (max-width: 450px) {
  h1 {
    font-size: 2.5em !important;
    width: 100%;
    margin-left: 400px !important;
  }
  input {
    width: 30% !important;
  }
  body {
    background: lightpink;
  }
}
</style>
