<template>
  <div id="app">
    <app-header></app-header>
    <ninjas />
    <app-footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import Ninjas from "./components/Ninjas";

export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    ninjas: Ninjas,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style>
body {
  font-family: monospace;
}
</style>
