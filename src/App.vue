<template>
  <div id="app">
    <Header />
    <router-view />
    <Newsletter v-if="$route.path != '/Contact'" />
    <slideout-panel></slideout-panel>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Newsletter from "./components/Newsletter.vue";

window.vue2PanelDebug = true;

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Newsletter,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Exo+2");
#app {
  background-color: #f8f8f8 !important;
  font-family: "Exo 2", sans-serif !important;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
