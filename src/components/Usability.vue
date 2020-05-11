// Usability.vue

<template>
  <div id ="provenance">
    <div v-show="bco" class="bco-stats">
      <th class="domain">Usability Domain</th>
        <table v-for="object in bco.usability_domain" :key="object">
          <tr>{{ object }}</tr>
        </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'usability',
  props: ['bco'],
}
</script>

<style></style