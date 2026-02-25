<template>
  <div>
    <h1>{{ msg }}</h1>
    <hr>
    <br>
    <label for="tempInput">
      Ingrese Temperatura °C
    </label>
    <input id="tempInput" v-model = "celsius">

      <p>
        Conv Temperatura °F: <b :style="{ color: colorTexto }">{{ fahrenheit }}</b>
      </p>
      <p>
        Conv Temperatura °K: <b :style="{ color: colorTexto }">{{ kelvin }}</b>
      </p>


  </div>
</template>

<script>
export default {
  name: 'ConversorVue',
  props: {
    msg: String
  },
  data() {
    return {
      celsius: ""
    }
  },
  computed: {

    fahrenheit() {
      let resultado = ""
      if (this.celsius !== null && this.celsius !== "") {
        resultado = ((parseFloat(this.celsius) * 9) / 5 + 32)
      }
      return resultado
    },

    kelvin() {
      let resultado = ""
      if (this.celsius !== null && this.celsius !== ""){
        resultado =  (parseFloat(this.celsius) + 273.15)
      }
      return resultado
    },
    colorTexto() {
      const temp = parseFloat(this.celsius)
      if (temp <= 0) {
        return 'blue'
      } else if (temp > 0 && temp < 15) {
        return 'magenta'
      } else {
        return 'red'
      }
    }
  }
}
</script>

<style scoped>
h1 {
  margin-bottom: 20px;
}

</style>