<template>
  <div id="demo7">




      <Clock>
        <span style="color:red;">เวลาปัจจุบัน</span>
      </Clock>

      <Clock>
        <span style="color:blue;">Timenow</span>
      </Clock>

      <Clock />




    <div class="vslot">
        <Clock>
            <span>เวลาปัจจุบัน 5555</span>
            
            <template v-slot:header>
                <h1>Header</h1>
            </template>
            <template v-slot:footer>
                <h3>Footer</h3>
            </template>

        </Clock>
    </div>



  </div>
</template>

<script>
import Clock from "../components/helper/Clock.vue";

export default {
  name: "Demo7",
  components: {
    Clock,
  },
};
</script>

<style scoped>
.vslot {
  color:magenta;
}
</style>
