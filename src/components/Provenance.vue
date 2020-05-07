// Provenance.vue

<template>
  <div>
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
</template>

<script>
export default {
  name: 'biocompute',
}
</script>

<style>
</style