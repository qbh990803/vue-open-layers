<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <OpenLayerMap />
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import OpenLayerMap from "@/views/map/OpenLayerMap.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    OpenLayerMap,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>

