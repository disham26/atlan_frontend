<template>
  <div id="app">
    <div id="nav">
      <b-navbar toggleable="lg" type="dark" variant="primary">
      <b-navbar-brand><router-link to="/"> Home </router-link></b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-item><router-link to="/task1">Task1&nbsp;</router-link></b-navbar-item>
        <b-navbar-item><router-link to="/task2">  Task2&nbsp; </router-link></b-navbar-item>
        <b-navbar-item><router-link to="/task3">  Task3 </router-link></b-navbar-item>
      </b-collapse>
      </b-navbar>
    </div>
    <router-view/>
    
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
