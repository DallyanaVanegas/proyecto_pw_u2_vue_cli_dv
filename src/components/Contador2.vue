<template>
  <!--HTML-->
  <h2>{{mostrarTitulo}}</h2>
  <p>{{ numero }} <sup>2</sup> = {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup> = {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup> = {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup> = {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup> = {{ obtenerCuadradoComputado }}</p>

  <div>
    <button v-on:click="incrementar">+1</button>
    <button v-on:click="decrementar">-1</button>
  </div>
</template>

<script>
export default {
  name: "Contador123",
  props:{
    titulo:String,
    inicio:{
      type:Number,
      required: false,
      default: 100,
      validator(value){
        //validacion q retorna true o false
        return value > 0 
      }
    }
  },
  data() {
    return {
      numero: this.inicio,
    };
  },
  methods: {
    obtenerCuadrado() {
      console.log("entro al metodo");
      return this.numero * this.numero;
    },
    incrementar() {
      return this.numero++;
    },
    decrementar() {
      return this.numero--;
    }
  },
  computed: {
    obtenerCuadradoComputado() {
      console.log("entro al metodo cuadrado computado");
      return this.numero * this.numero;
    },
    mostrarTitulo(){
      return this.titulo || 'Titulo Vacio 2'
    }
  },
};
</script>

<style>
button {
  background-color: #64bb87;
  border-radius: 5px;
  color: white;
  margin: 0 5px;
  cursor: pointer;
}
button:hover {
  background-color: #5a68a6;
  transition: 0.3s ease-in-out;
}
</style>