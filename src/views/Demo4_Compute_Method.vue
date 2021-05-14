<template>
  <div id="demo4">
      <h1 class="A1">
          Data from Compute : {{fullname}}
      </h1>
    <h2>{{firstname}}\n{{lastname}}</h2>

      <h1 class="A1">
          Random Data from Compute : {{getrandom}}
      </h1>
      <h1 class="A1">
          Random Data from Compute : {{getrandom}}
      </h1>
      <h1 class="A1">
          Random Data from Compute : {{getrandom}}
      </h1>


      <h1 class="B1">
          Random Data from Method : {{getrandom1()}}
      </h1>
      <h1 class="B1">
          Random Data from Method : {{getrandom1()}}
      </h1>
      <h1 class="B1">
          Random Data from Method : {{getrandom1()}}
      </h1>


  </div>
</template>

<script>
export default {
    name:"Demo4",
    data(){
        return{
            firstname:"Teerapat",
            lastname:"Sinlapawisan"
        }
    },
    computed:{
        getrandom(){
            return Math.random()
        },
        fullname(){
            return this.firstname + " " + this.lastname
        }

    },
    methods:{
        getrandom1(){
            return Math.random()
        }
    }
}
</script>

<style scoped>
.A1{
    color: red;
}
.B1{
    color: rgb(143, 247, 8);
}

</style>