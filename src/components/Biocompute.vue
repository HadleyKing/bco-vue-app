// Biocompute.vue

<template>
    <div id="biocompute">
        <div v-show="bco" class="bco-stats">
            <th class="domain">Top Level</th>
            <tr>
                <td>BioCompute ID:</td><td>{{ bco.object_id }}</td>
            </tr>
            <tr>
                <td>E-Tag</td><td>{{bco.etag}}</td>
            </tr>
            <tr>
                <td>Spec Version</td>
                <td>{{bco.spec_version}}</td>
                <td><button v-on:click="editField">Edit</button></td>
            </tr>
        </div>
     </div>
</template>

<script>

    export default {
        name: 'biocompute',
        props: ['bco'],
        methods: {
          editField: function (event) {
            // `this` inside methods points to the Vue instance
            alert('Hello ' + this.name + '!')
            // `event` is the native DOM event
            if (event) {
              alert(event.target.tagName)
            }
          }
        }
    }
</script>

<style>
</style>