<template>
    <div id="header">
    <ul>
    <li><router-link to="/"><button>Home</button></router-link></li>
    <li><router-link to="/longdo"><button>longdo maps</button></router-link></li>
    <li><router-link to="/demo1"><button>Demo1</button></router-link></li>
    <li><router-link to="/demo2"><button>Demo2 Event</button></router-link></li>
    <li><router-link to="/demo3"><button>Demo3 Data</button></router-link></li>
    <li><router-link to="/demo4"><button>Demo4 Compute&Method</button></router-link></li>
    <li><router-link to="/demo5"><button>Demo5 Binding</button></router-link></li>
    <li><router-link to="/demo6"><button>Demo6 Form & V-model</button></router-link></li>
    <li><router-link to="/demo7"><button>Demo7 Slot</button></router-link></li>
    <li><router-link to="/demo8"><button>Demo8 Condition</button></router-link></li>
    <li><router-link to="/demo9"><button>Demo9 Loop</button></router-link></li>
                                                 
    </ul>
    </div>
</template>

<script>
export default {
    name:"Header",
}
</script>

<style scoped>
    ul{
    margin: 0;
    padding: 0;
    }
    li{
    display: inline;
    margin-right: 5px;
    }
</style>