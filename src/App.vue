<template>
  <div id="app">
    <h3>{{title}}</h3>
    <img src="./assets/logo.png" />
    <p>{{greeting('morning')}}</p>
    <ninjas />
    <weapons />
  </div>
</template>

<script>
import Weapons from "./Weapons.vue";

export default {
  components: {
    weapons: Weapons,
  },
  data() {
    return {
      title: "My First Vue File",
    };
  },
  methods: {
    greeting: (time) => {
      return `Good ${time}`;
    },
  },
};
</script>

<style>
h3 {
  color: purple;
}
</style>
