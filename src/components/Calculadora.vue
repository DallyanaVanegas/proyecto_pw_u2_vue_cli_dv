<template>
  <!--HTML-->
  <h2>Calculadora</h2>

  <table>
    <tr>
      <td>
        <label for="num1">Primer número:</label>
      </td>
      <td>
        <input type="text" id="num1" v-model="num1" />
      </td>
    </tr>
    <tr>
      <td>
        <label for="num2">Segundo número:</label>
      </td>
      <td>
        <input type="text" id="num2" v-model="num2" />
      </td>
    </tr>
  </table>

  <div>
    <button v-on:click="sumar()">+</button>
    <button v-on:click="restar()">-</button>
    <button v-on:click="dividir()">/</button>
    <button v-on:click="multiplicar()">x</button>
  </div>

  <table>
    <tr>
      <td>
        <label for="sol"> Sol:</label>
      </td>
      <td>
        <div>
          <p>{{obtenerSol}}</p>
        </div>
      </td>
    </tr>
  </table>
</template>

<script>
export default {
  name: "calcu",
  data() {
    return {
      num1: "",
      num2: "",
      sol: "_____",
    };
  },
  methods: {
    sumar() {
      this.sol = parseInt(this.num1) + parseInt(this.num2);
    },
    restar() {
      this.sol = parseInt(this.num1) - parseInt(this.num2);
    },
    dividir() {
      this.sol = parseInt(this.num1) / parseInt(this.num2);
    },
    multiplicar() {
      this.sol = parseInt(this.num1) * parseInt(this.num2);
    },
  },
  computed: {
    obtenerSol() {
      return this.sol;
    },
  },
};
</script>

<style scoped>
#div1 {
  margin: 10px;
}
button {
  background-color: #4caf50;

  color: white;
  padding: 2px 20px;
  text-align: center;
  display: inline-block;
  font-size: 16px;
  margin: 8px 2px;
  cursor: pointer;
}
button:hover {
  background-color: #5a68a6;
  transition: 0.3s ease-in-out;
}

button:active {
  transform: translateY(5px);
}

table {
  margin: auto;
  text-align: right;
}
</style>