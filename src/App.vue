<template>
  <div id="app">
      <NavBar>
        <b-nav-item to="/" exact>Home</b-nav-item>
        <b-nav-item to="/about" exact>About</b-nav-item>
      </NavBar>
    <router-view/>
  </div>
</template>

<script>
  import NavBar from '@/components/NavBar.vue'

  export default {
    components: {
      NavBar
    }
  }
</script>

<style lang="scss">
@import "sass/app";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
