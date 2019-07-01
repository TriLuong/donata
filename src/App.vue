<template>
  <div id="app">
    <Home />
    <Event />
    <Collection />
  </div>
</template>

<script>
import Home from "./layouts/Home"
import Event from "./layouts/Event"
import Collection from "./layouts/Collection"

export default {
  name: 'app',
  components: {
    Home,
    Event,
    Collection
  },
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
