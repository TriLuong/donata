<template>
  <div id="app">
    <Home />
    <Event />
    <Collection />
    <Public />
    <Footer />
  </div>
</template>

<script>
import Home from "./layouts/Home"
import Event from "./layouts/Event"
import Collection from "./layouts/Collection"
import Public from "./layouts/Public"
import Footer from "./layouts/Footer"

export default {
  name: 'app',
  components: {
    Home,
    Event,
    Collection,
    Public,
    Footer
  },
}
</script>

<style>
*{
  box-sizing: border-box;
  font-family: "Lato";
  margin: 0 ;
  padding: 0;
}
.row {
  margin: 0 !important;
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
