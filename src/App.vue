<template>
<!-- wait to melt component -->
  <div id="app">
    <Header/>

    <router-view></router-view>

  <Footer @tricker007="tricker007" :customText="testText"/>
  <span class="clock">{{text}}</span>
  </div>
</template>

<script>
import Header from "../src/components/layout/Header.vue"
import Footer from "@/components/layout/Footer.vue"
export default {
  name: "app",
  components:{
    Header,
    Footer
  },
  data(){
    return{
      testText:"test Text from data",
      text:""
    }
  },
  methods: {
    tricker007(event){
      this.text = event
    }
  },
};
</script>



<style>
.contentli{
  color:red
}
.clock{
  font-size: 10px;
}
</style>