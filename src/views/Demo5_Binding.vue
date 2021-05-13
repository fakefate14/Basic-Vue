<template>
  <div id="demo5">
    <h1>Binding</h1>
    <img :src="imageURL" :height="height_data" />
    <img src="https://www.codemobiles.com/biz/images/codemobiles_logo.svg?ref=10" />
    <a v-bind:href="FB">My Facebook</a>

    <div :class="[errorClass,importantClass]">CodeMobiles</div>
    <div :class="[false ? errorClass:importantClass]" :style="{color:ColorX}">CodeMobiles</div>
    <span :style="isTrue ? styleObs:''">{{isTrue}}</span>
    <button @click="booleanTest()">ToggleButton</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageURL:
        "https://www.codemobiles.com/biz/images/codemobiles_logo.svg?ref=10",
      height_data: "20",
      FB: "https://www.facebook.com/Fakefate14/",
      errorClass: "TestTest",
      importantClass: "IMIM",
      ColorX: "green",
      styleObs: {
        backgroundColor: "yellow",
        color: "red",
      },isTrue:true

    };
  },
  methods: {
    booleanTest(){
        this.isTrue = !this.isTrue
        console.log("Test")
    },
  },
};
</script>

<style scoped>
.TestTest {
  color: red;
}
.IMIM {
  font-weight: 900;
}
</style>