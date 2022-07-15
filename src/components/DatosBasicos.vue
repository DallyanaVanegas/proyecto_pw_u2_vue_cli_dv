<template>

  <label>Nombre {{nombre}}:</label>
  <input type="text">

  <label>Apellido {{apellido}}:</label>
  <input type="text">

  <label>Correo {{correo}}:</label>
  <input type="text">
</template>

<script>
export default {
  name: "datosBasicos",
  props:{
    nombre:String,
    apellido:String,
    correo:String,
    type:String,
  },
    
  data() {
    return {
      numero: this.inicio,
    };
  },
  computed: {
    
  },
};
</script>

<style scoped>
label{
    display: block;
}
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