<template>
  <div id="demo6">
    <form>
      <!-- Firstname -->
      <div>
        <label for="first_name">Firstname</label>
        <input v-model="applicant.first_name" type="text" name="first_name" id="first_name" />
      </div>

      <!-- Lastname --123456>
      <div>
        <label for="last_name">Lastname</label>
        <input v-model="applicant.last_name" type="text" name="last_name" id="last_name" />
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
          <option value="react">react</option>
          <option value="vue">vue</option>
          <option value="angular">angular</option>
          <option value="python">python</option>
          <option value="R">R</option>
        </select>
      </div>



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
      },
    };
  },
};
</script>

<style>
</style>