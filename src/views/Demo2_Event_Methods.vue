<template>
  <div id="demo2">
    <h1>Event & Method</h1>
    <button v-on:click="clickMe()">click</button>
    <button v-on:click="clickMe2('welcome to vue.js')">click2</button>
    <button @click="clickMe3('welcome to vue.js')">click3</button>
    <h3>{{ getTime() }}</h3>
  </div>
</template>

<script>
export default {
  name: "demo2",
  methods: {
    clickMe() {
      alert("Hi");
    },
    clickMe2(val) {
      alert("Hi" + " " + val);
    },
    clickMe3(val) {
      alert("Hi !!!" + " " + val);
    },
    getTime() {
      return Date();
    },
    initial(){
        console.log("Initialization")
    }
  },
  mounted() {
    this.initial()
    console.log(true)
  },
};
</script>

<style>
button {
  margin-right: 5px;
}
</style>
