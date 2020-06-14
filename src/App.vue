<template>
  <div id="app">
 <NavBar/>
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
</template>

<script>

  // Components
  import NavBar from "./view/components/NavBar/NavBar";

export default {
  name: 'App',
  components: {
      NavBar
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
</style>
