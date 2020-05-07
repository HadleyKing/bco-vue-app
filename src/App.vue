// App.vue 

<template>
  <div id="app">
    <img alt="BCO logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your BCO-Vue-App"/>
    <h1>BioCompute Object</h1>
    <button v-on:click="getBCO">Show BioCompute Object</button>
    <biocompute :bco="bco" />

  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import Biocompute from './components/Biocompute.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    Biocompute,
  },
  data() {
    return {
      bco: {}
    };
  },
  methods: {
    getBCO() {
      fetch("data.json")
        .then(response => response.json())
        .then(data => (this.bco = data));
    }
  }
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
</style>
