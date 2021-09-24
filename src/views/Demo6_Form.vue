<template>
  <div id="demo6">
    <form v-on:submit.prevent="submit">
      <div style="margin-top: 10px;">
        <label for="firstname">Firstname</label>
        <input type="text" name="first_name" v-model.trim="applicant.firstname" />
      </div>

      <div style="margin-top: 10px;">
        <label for="lastname">Lastname</label>
        <input type="text" name="last_name" v-model.trim="applicant.lastname" />
      </div>

      <div>
        <label for="sex">Male</label>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />

        <label for="sex">Female</label>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>

      <div>
          <label for="age">Age</label>
          <input type="number" v-model.number="applicant.age">
      </div>

      <div>
        <select name="courses" v-model="applicant.course">
          <option value="react">React</option>
          <option value="angular">Angular</option>
          <option value="vuejs">VueJS</option>
        </select>
      </div>

      <div>
        <button type="button" @click.exact="clear" @click.alt="useDefault">Clear</button>
        <button type="submit">Submit</button>
      </div>
    </form>

    <div style="margin-top: 16px; color: red;">
      #Spy {{ JSON.stringify(applicant) }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Demo6",
  data() {
    return {
      applicant: {
        firstname: "",
        lastname: "",
        sex: "male",
        age:0,
        course: "",
      },
    };
  },
  methods: {
    submit() {
    //   event.preventDefault();
      alert(JSON.stringify(this.applicant));
    },
    clear() {
      this.applicant = {
        firstname: "",
        lastname: "",
        sex: "male",
        age:0,
        course: "",
      };
    },
    useDefault() {
      this.applicant = {
        firstname: "xxxx",
        lastname: "xxxx",
        sex: "male",
        age:0,
        course: "react",
      };
    },
  },
};
</script>

<style></style>
