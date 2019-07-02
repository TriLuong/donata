<template>
  <div id="app">
    <Home />
    <Event />
    <Collection />
    <Public />
  </div>
</template>

<script>
import Home from "./layouts/Home"
import Event from "./layouts/Event"
import Collection from "./layouts/Collection"
import Public from "./layouts/Public"

export default {
  name: 'app',
  components: {
    Home,
    Event,
    Collection,
    Public
  },
}
</script>

<style>
*{
  box-sizing: border-box;
  font-family: "Lato";
  margin: 0;
  padding:0;
  overflow-x: hidden;
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
