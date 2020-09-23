<template>
  <div id="ninjas">
    <ul>
      <li v-for="(ninja,index) in ninjas" v-bind:key="index" @click="ninja.show = !ninja.show">
        <h2>{{ninja.name}}</h2>
        <h3 v-show="ninja.show">{{ninja.speciality}}</h3>
      </li>
    </ul>
    <button @click="click">Methods</button>
    <button @click="tesComp">Computed</button>
  </div>
</template>
<script>
export default {
  props: {
    ninjas: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {};
  },
  methods: {
    click: function () {
      console.log("anda menekan click");
    },
  },
  // computed: {
  //   tesComp: function () {
  //     return console.log("anda menggunakan computed");
  //   },
  // beforeCreate() {
  //   alert("before create");
  // },
  // created() {
  //   alert("created");
  // },
  // beforeMount() {
  //   alert("before mount");
  // },
  // mounted() {
  //   alert("mounted");
  // },
  // beforeUpdate() {
  //   alert("before update");
  // },
  // updated() {
  //   alert("updated");
  // },
};
</script>
<style scoped>
#ninjas {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
}
</style>