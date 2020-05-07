// Biocompute.vue

<template>
  <div>
    <div v-show="bco" class="bco-stats">
      <thread class="domain">Top Level</thread>
      <tr>
          <td>BioCompute ID:</td><td>{{ bco.bco_id }}</td>
      </tr>
      <tr>
          <td>E-Tag</td><td>{{bco.checksum}}</td>
      </tr>
      <tr>
        <td>Spec Version</td><td>{{bco.bco_spec_version}}</td>
      </tr>
    </div>
  </div>
</template>

<script>
export default {
  name: 'biocompute',
  props: ['bco'],
}
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
</style>