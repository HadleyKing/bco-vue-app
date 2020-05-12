// Contributors.vue

<template >
  <div id ="contributors">
    <div v-show="bco" class="bco-stats">
      <th class="domain">Contributors</th>
        <table v-for="object in bco.contributors" :key="object">
          <tr>{{ object }}</tr>
        </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'contributors',
  props: ['bco'],
}
</script>

<style></style