<template>
  <div>
    <h3>List of weapons</h3>
    <ol>
      <li v-for="weapon in weapons">{{weapon}}</li>
    </ol>
  </div>
</template>
<script>
export default {
  data() {
    return {
      weapons: ["Suriken", "Kunai", "Bomb Paper"],
    };
  },
};
</script>
<style scoped>
h3 {
  color: gold;
}
</style>