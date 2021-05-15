<template>
  <div id="app">


    <Header />


    <Content/>



    <Footer v-on:Tricker001="Tricker001" :customText="testText" />
    <span class="clock">{{text}}</span>


  </div>
</template>

<script>
import Header from "../src/components/layout/Header.vue";
import Footer from "@/components/layout/Footer.vue";
import moment from "moment";
import Content from "../src/components/layout/Content"


export default {
  name: "app",
  components: {
    Header,
    Footer,
    Content
  },
  data() {
    return {
      testText: "test Text from data",
      text: "123",
    };
  },
  methods: {
    Tricker001(event) {
      this.text = moment(event).format("MM/DD/YYYY hh:mm:ss");
    },
  },
};
</script>



<style scoped>
.contentli {
  color: red;
}
.clock {
  font-size: 10px;
}

</style>