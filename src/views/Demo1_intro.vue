<template>
  <div id="demo1">
    <h1>Demo1</h1>
    <h1>v-model</h1>
    <!-- MVVM -->
    <input v-model="message" type="text" placeholder="enter your message" name id />
    <button @click="reset()">Reset</button>
    <div>
      <span>{{message}}</span>
    </div>

  </div>
</template>

<script>
export default {
  name: "demo1",
  data(){
      return{
          message:""
      }
  },
  methods:{
      reset(){
          this.message = ""
      }
  }
};
</script>

<style></style>
