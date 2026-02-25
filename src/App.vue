<template>
  <Conversor msg="Conversor de Temperatura"/>
  <br>
  <hr>
  <Respuestas />
</template>

<script>
import Conversor from './components/Conversor.vue'
import Respuestas from './components/Respuestas.vue';

export default {
  name: 'App',
  components: {
    Conversor,
    Respuestas
  }
}
</script>

<style>
#app {
  font-family: 'Times New Roman', Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
