<template>
  <Conversor msg="Conversor de Temperatura"/>
  <br>
  <hr>
  <p>Respuestas: 1:C - 2:B - 3:C - 4:A</p>
</template>

<script>
import Conversor from './components/Conversor.vue'

export default {
  name: 'App',
  components: {
    Conversor
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
