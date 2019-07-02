<template>
  <div class="home">
    <img alt="Vue logo" class="image" src="../assets/atlan-blue.svg">
    <h1>First task- Email follow ups</h1>
    <b-list-group>
  <b-list-group-item v-for="(email,index) in emails" style="text-align:left" v-bind:key="index">
      <h5>{{email.about}}</h5>
      Subject : <b>{{email.subject}}</b><br>
      Body : <pre>{{email.body}}</pre>
  </b-list-group-item>
  
</b-list-group>
  </div>
</template>

<script>
// @ is an alias to /src
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)

export default {
  name: 'task1',
  data() {
      return {
        emails: [
        ]
      }
    },
    created : function(){
        var _this=this
        Vue.axios
        .get('http://localhost:8000/task1')
        .then(response => {
          _this.emails=response.data,
          console.log(_this.emails)

      })
    }
}
</script>
<style>
.image{
  width:30%
}</style>