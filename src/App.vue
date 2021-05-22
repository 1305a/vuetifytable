<template>
  <v-app>
    <v-data-table
      :headers="headers"
      :items="tableFunction"
      :items-per-page="10"
      class="elevation-1"
    >
    </v-data-table>
  </v-app>
</template>

<script>

import tableJson from '@/table.json';

export default {
  name: 'App',

  components: {
  },
  data() {
    return {
      headers: [{text:'NAME',value: 'name', width: '17rem'},
      {text:'DESCRIPTION',value: 'description', width: '45%'},
      {text:'MIME TYPE',value: 'mime_type', width: '27%'},
      {text:'OPEN MODE',value: 'open_mode', width: '10.3rem'}
      ]
    }
  },
  computed: {
    tableFunction() {
      return tableJson
    }
    
  },
  methods: {
    tableFunctionMethods() {
      console.log(this.tableFunction)
    }
  }
}
</script>
