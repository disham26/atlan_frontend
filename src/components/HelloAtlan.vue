<template>
  <div class="hello">
    <b-container>
      <p>
        Here you can type a query and get the list of the tables on the go.   
      </p>
    </b-container>
    <br><br>
    <b-container>
      <b-form-input class="mx-auto" v-model="query" placeholder="Enter the query"></b-form-input>
    </b-container>
    <br><br>
    <b-container>
      <b-button @click="showTables">Get Table Names</b-button>
    </b-container>
    <br><br>
    <b-container>
      <b-list-group>
        <b-list-group-item class="table_list" v-for="(table,index) in tables" v-bind:key="index">{{table}}</b-list-group-item><br>
      </b-list-group>
    </b-container>
  </div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)

export default {
    name: 'HelloAtlan',
  data() {
      return {
        query: '',
        tables: [
        ]
      }
    },
    methods: {
      showTables: function(){
        var _this=this
        Vue.axios
        .get('http://localhost:8000/task3?query='+this.query)
        .then(response => {
          _this.tables=response.data.text
      })
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
