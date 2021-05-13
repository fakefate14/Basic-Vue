<template>
  <div id="demo3">
      <h1>Data & Variable</h1>
      <button v-on:click="plus()">Count++</button>
      <span>{{count}}</span>
      <div>{{message}}</div>
      <div>{{isLogged}}</div>

      <input v-model="values" type="text" placeholder="please input data">
    <span>{{values}}</span>
    <div v-if="values == 'test'">Yahoo !</div>

    <div>{{account}} {{account.username}} {{account.password}}</div>
    <div>{{account.arr}}</div>

    <ul>
        <li class="contentli"  v-for="(item,index) in account.arr" :key="index">{{index+1}}. {{item}}</li>
    </ul>

    <div>
        <span class="title">1234</span>
    </div>
  </div>
</template>

<script>
export default {
    name:"demo3",
    data(){
        return{
            count:0,
            message:"",
            isLogged:false,
            values:null,
            account:{
                username:"admin",
                password:"1234",
                arr:[
                    "angulat","Vue","React"

                ]
            }
        }
    },
    methods:{
        plus(){
            this.count = this.count + 1
            this.isLogged = !this.isLogged
            this.values = null
        }
    },
    mounted() {
        this.message = "initial_message"
    },
}
</script>

<style scoped>
/* li{
    color: red;
} */
.title{
    font-size:50px;
    color: rosybrown;
}
</style>