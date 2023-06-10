<template>
  <div id="app">
    <h1>Reuniones</h1>
    <ListaUsuarios></ListaUsuarios>
    <OtrosUsuarios></OtrosUsuarios>
    <MasUsuario></MasUsuario>
  </div>
</template>

<script>
import ListaUsuarios from './components/ListaUsuarios.vue';
import OtrosUsuarios from './components/OtrosUsuarios.vue'; 
import MasUsuario from './components/MasUsuario.vue';

 
export default {
  name: 'App',
  components: {
    ListaUsuarios,
    OtrosUsuarios,
    MasUsuario
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
</style>
