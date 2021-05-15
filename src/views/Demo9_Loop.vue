<template>
  <div id="demo9">
    <h1>Loop</h1>

    <ul>
      <li v-for="(item, index) in ['A', 'B', 'C']" :key="index">{{ item }}</li>
    </ul>
    <hr />

    <ul>
      <li v-for="(item, index) in mycourse" :key="index">{{ item }}</li>
    </ul>
    <hr />

    <ul>
      <li v-for="(item, index) in mCourses" :key="index">{{ item.title }} : {{ item.price }}</li>
    </ul>
    <hr />

    <ul>
      <li v-for="({title,price}, index) in mCourses" :key="index">{{ title }} : {{ price }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo9",
  data() {
    return {
      mycourse: ["iOS", "Android", "Flutter"],
      mCourses: [{ title: "iOS" , price:100}, { title: "Android" , price:200}, { title: "Flutter" , price:300}],
    };
  },
};
</script>

<style></style>
