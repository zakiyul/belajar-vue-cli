<template>
  <div id="app">
    <!-- <app-header v-bind:title="title" @changeTitle="updateTitle" />
    <ninjas v-bind:ninjas="ninjas" />
    <button @click="deleteNinja">Delete Ninja</button>
    <app-footer v-bind:title="title" />-->
    <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>
    <button @click="handleformOne">form one</button>
    <button @click="handleformTwo">form two</button>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import Ninjas from "./components/Ninjas";
import FormHelper from "./components/FormHelper";
import FormOne from "./components/FormOne";
import FormTwo from "./components/FormTwo";

export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    ninjas: Ninjas,
    "form-helper": FormHelper,
    "form-one": FormOne,
    "form-two": FormTwo,
  },
  data() {
    return {
      title: "Vue Ninja",
      component: "form-one",
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
    handleformOne: function () {
      this.component = "form-one";
    },
    handleformTwo: function () {
      this.component = "form-two";
    },
  },
};
</script>
<style>
body {
  font-family: "Courier New", Courier, monospace;
}
</style>
