<template>
  <ul>
    <li v-for="weapon in weapons">{{weapon}}</li>
  </ul>
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