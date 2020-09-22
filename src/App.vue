<template>
  <div id="app">
    <app-header v-bind:title="title" @changeTitle="updateTitle" />
    <ninjas v-bind:ninjas="ninjas" />
    <button @click="deleteNinja">Delete Ninja</button>
    <app-footer v-bind:title="title" />
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
    return {
      title: "Vue Ninja",
      ninjas: [
        { name: "Ryu", speciality: "Vue Components", show: false },
        { name: "Crystal", speciality: "HTML Wizardry", show: false },
        { name: "Hitoshi", speciality: "Click Event", show: false },
        { name: "Tango", speciality: "Conditionals", show: false },
        { name: "Kami", speciality: "Webpack", show: false },
        { name: "Yoshi", speciality: "Data Digging", show: false },
      ],
    };
  },
  methods: {
    updateTitle: function (updatedTitle) {
      this.title = updatedTitle;
    },
    deleteNinja: function () {
      this.ninjas.pop();
    },
  },
};
</script>
<style>
body {
  font-family: "Courier New", Courier, monospace;
}
</style>
