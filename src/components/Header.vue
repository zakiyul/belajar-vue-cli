<template>
  <div>
    <header>
      <h1 @click="changeTitle">{{title}}</h1>
    </header>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
  data() {
    return {};
  },
  methods: {
    changeTitle: function () {
      this.$emit("changeTitle", "Vue Wizard");
    },
  },
};
</script>
<style scoped>
header {
  background-color: lightgreen;
  padding: 10px;
}
h1 {
  color: #222;
  text-align: center;
}
</style>