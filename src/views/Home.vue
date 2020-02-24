<template>
  <div class="container">
    <img class="logo" alt="OpenUBI Project logo" src="../assets/open-ubi-project-logo.svg">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>

<style>
.logo {
  height: 10em;
}
</style>