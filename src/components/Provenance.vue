// Provenance.vue

<template>
  <div id ="provenance">
    <div v-show="bco" class="bco-stats">
      <th class="domain">Provenance Domain</th>
      <tr>
        <td>Name</td><td>{{bco.provenance_domain.name}}</td>
      </tr>
      <tr>
        <td>Version</td><td>{{bco.provenance_domain.version}}</td>
      </tr>
      <tr>
        <td>Review</td><td>{{bco.provenance_domain.review}}</td>
      </tr>
      <tr>
        <td>Obsolete</td><td>{{bco.provenance_domain.obsolete_after}}</td>
      </tr>
      <tr>
        <td>Embargo</td><td>{{bco.provenance_domain.embargo}}</td>
      </tr>
      <tr>
        <td>Created:</td><td>{{bco.provenance_domain.created}}</td>
      </tr>
      <tr>
        <td>Modified</td><td>{{bco.provenance_domain.modified}}</td>
      </tr>
      <tr>
        <td>Contributors</td><td>{{bco.provenance_domain.contributors}}</td>
      </tr>
      <tr>
        <td>License</td><td>{{bco.provenance_domain.license}}</td>
      </tr>
    </div>
  </div>
</template>

<script>
export default {
  name: 'provenance',
  props: ['bco'],
}
</script>

<style>
</style