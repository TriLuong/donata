<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import NavBar from "./components/NavBar"
import Home from "./layouts/Home"

export default {
  name: 'app',
  components: {
    Home
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  font-family: "Lato";
}
@font-face {
  font-family: "Lato";
  src: url("./assets/00-Fonts/Lato/Lato-Regular.ttf");
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
