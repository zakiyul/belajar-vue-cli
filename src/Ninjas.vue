<template>
  <div>
    <h3>List of ninjas</h3>
    <ul>
      <li v-for="ninja in ninjas" v-bind:key="ninja">{{ninja}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      ninjas: ["Yoshi", "Mario", "Ryu"],
    };
  },
};
</script>
<style scoped>
h3 {
  color: maroon;
}
</style>