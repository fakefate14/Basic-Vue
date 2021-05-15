<template>
  <div id="demo8">
      <h1>Condition</h1>

    <div v-if="type==='A'">
        I'm A
    </div>
    <div v-else-if="type==='B'">
        I'm B
    </div>
    <div v-else-if="type==='C'">
        I'm C
    </div>
    <div v-else>
        I'm  NOT A B C
    </div>

    <div v-if="isShow">
        Blink !!!!!
    </div>
    <div v-else>
        <br>
    </div>


<br>
<div>
    <button v-on:Click="ChageAlphabet()">Chage</button>
</div>
</div>
</template>

<script>
export default {
    name:"Condition",
    data(){
        return{
        type:"A",
        isShow:false
    }},
    mounted(){
        setInterval(() => {
            this.isShow = !this.isShow
        }, 1000);
    },
    methods:{
        ChageAlphabet(){
            if(this.type=="A"){
                this.type = "B"
            }else if(this.type=="B"){
                this.type = "C"
            }else if(this.type == "C"){
                this.type = "D"
            }else{
                this.type = "A"
            }
        }
    }
}
</script>

<style>

</style>