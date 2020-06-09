<template>
  <div id="app">
      <div class="navbar-wrapper mb-4">
          <NavBar>
              <b-nav-item to="/" exact>Home</b-nav-item>
              <b-nav-item to="/mission" exact>Mission</b-nav-item>
              <b-nav-item to="/scope" exact>Project Scope</b-nav-item>
              <b-nav-item to="/about" exact>About</b-nav-item>
          </NavBar>
      </div>
      <div class="container">
          <router-view/>
      </div>
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
</style>
