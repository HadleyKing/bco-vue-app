// TopLevel.vue

<template>
  <div>
    <button v-on:click="getBCO">Show BioCompute Object</button>
    <div v-show="bco" class="bco-stats">
      <thread class="domain">Top Level</thread>
      <tr>
          <td>BioCompute ID:</td><td>{{bco.bco_id}}</td>
      </tr>
      <tr>
          <td>E-Tag</td><td>{{bco.checksum}}</td>
      </tr>
      <tr>
        <td>Spec Version</td><td>{{bco.bco_spec_version}}</td>
      </tr>
    </div>
  </div>
<template>

<script>
  export default {
    name: 'top-level',
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
},
</script>

<style>
</style