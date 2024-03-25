<template>
  <div>
    <h4>Bienvenido/a</h4>
    <Home first-name="Nora" last-name="Vazquez"></Home>
  </div>
</template>

<script>
import Home from './components/Home.vue'
import { provide, ref } from "vue";
export default {
  name: 'App',
  components: {
    Home,
  },
  setup() {
    const username = ref("noraxx");
    provide("username", username);
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
