<template>
  <img src="./assets/logo.png" alt="Logo" />
  <Etudiant nom="Conde" prenom="Kaba" age=54 />
</template>

<script>
import Etudiant  from './components/Etudiant.vue'

export default {
  name: 'App',
  components: {
    Etudiant
  },
 
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
</style>
