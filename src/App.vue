// App.vue 

<template>
  <div id="app" class="container">
    <img alt="BCO logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to the BCO-Vue-App"/>
    <h1>BioCompute Object</h1>
    <button v-on:click="getBCO">Show BioCompute Object</button>
    <div class="domain">
        <biocompute :bco="bco" />
    </div>
    <usability :bco="bco" />
    <provenance :bco="bco" />
    <parametric :bco="bco" />
  </div>
</template>

<script>
    import axios from 'axios'
    import HelloWorld from './components/HelloWorld.vue'
    import Biocompute from './components/Biocompute.vue'
    import Usability from './components/Usability.vue'
    import Provenance from './components/Provenance.vue'
    import Parametric from './components/Parametric.vue'

export default {
    name: 'App',
    components: {
        HelloWorld,
        Biocompute,
        Provenance,
        Usability,
        Parametric,
    },
    data() {
        return {
            bco: {}
        }
    },
    methods: {
        getBCO() {
            axios.get("https://raw.githubusercontent.com/biocompute-objects/BCO_Specification/1.4.0/examples/HCV1a.json")
            .then(response => (this.bco = response.data));
        },
    }
};
</script>

<style>
.bco-data {
  display: flex;
  align-items: center;
  margin-top: 20px;
  margin-left: 20px;
  border-bottom: 2px solid #ccc;
  padding: 20px;
}

.bco-icon {
  flex-grow: 1;
}

.bco-stats {
  flex-grow: 8;
  text-align: left;
  padding-left: 20px;
}

.bco-stats .domain {
  font-size: 30px;
}

.bco-temp {
  flex-grow: 1;
  font-size: 35px;
}

img {
  width: 70px;
}

button {
    padding:10px;
    background-color: #1aa832;
    color: white;
    border: 1px solid #ccc;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
