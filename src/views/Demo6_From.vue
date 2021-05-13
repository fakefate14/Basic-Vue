<template>
  <div id="demo6">
    <!-- can use with submit.prevent -->
    <form @submit="submit">
      <!-- Firstname -->
      <div>
        <label for="first_name">Firstname</label>
        <input v-model.trim="applicant.first_name" type="text" name="first_name" id="first_name" />
      </div>

      <!-- Lastname -->
      <div>
        <label for="last_name">Lastname</label>
        <input v-model.lazy="applicant.last_name" type="text" name="last_name" id="last_name" />
      </div>

      <!-- Age -->
      <div>
        <label for="age">Age</label>
        <input v-model.number="applicant.age" type="number" name="last_name" id="last_name" />
      </div>


      <!-- Sex -->
      <div>
        <label for="sex">Male</label>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />
        <label for="sex">Female</label>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>





      <!-- Course/// -->
      <div>
        <select name="course" v-model="applicant.course">
          <option value="React">React</option>
          <option value="Vue">Vue</option>
          <option value="Angular">Angular</option>
          <option value="Python">Python</option>
          <option value="R">R</option>
        </select>
      </div>

      <button type="button" @click.exact="Clear()" @click.alt="useDefault()">Clear</button>
      <button type="submit">Submit</button>
    </form>

    <!-- Spy -->
    <div style="margin-top:16px; color:red;">{{applicant}}</div>
    <div style="margin-top:16px; color:red;">{{JSON.stringify(applicant)}}</div>
  </div>
</template>

<script>
export default {
  name: "demo6",
  data() {
    return {
      applicant: {
        first_name: "",
        last_name: "",
        sex: "male",
        course: "react",
        age:null
      },
    };
  },
  methods: {
    Clear() {
      console.log("clear data");
      this.applicant = {
        first_name: "",
        last_name: "",
        sex: "male",
        course: "react",
        age:null
      };
    },
    submit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.applicant));
    },

  },
};
</script>

<style>
</style>