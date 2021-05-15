<template>
  <div id="footer" class="footer">
    <span :style="{color}">{{customText}}</span>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props:["customText","color"],
  mounted(){

    setInterval(() => {
      this.$emit('Tricker001', Date());
    }, 100);

    
  }
};
</script>

<style scoped>
.footer {
  font-size: 12px;
  color: gray;
  padding-top:16px ;
}
</style>