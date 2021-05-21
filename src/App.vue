<template>
  <v-app>
   <v-btn
   @click ="tableFunctionMethods"
   >
   Кнопка
   </v-btn>
   <div
    v-for="item in tableFunction"
    :key="item.id"
   >
   {{item.name}}
   </div>
  </v-app>
</template>

<script>

import tableJson from '@/table.json';

export default {
  name: 'App',

  components: {
  },
  computed: {
    tableFunction() {
      return tableJson
      //tableData = tableJson
    }
    
  },
  methods: {
    tableFunctionMethods() {
      console.log(this.tableFunction)
    }
  }
}
</script>
