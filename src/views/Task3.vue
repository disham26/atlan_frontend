<template>
  <div class="home">
    <img alt="Vue logo" class="image" src="../assets/atlan-blue.svg">
    <h1>Third task- SQL parser</h1>
    <HelloAtlan msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloAtlan from '@/components/HelloAtlan.vue'

export default {
  name: 'home',
  components: {
    HelloAtlan
  }
}
</script>
<style>
.image{
  width:30%
}</style>