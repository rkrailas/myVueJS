<template lang="">
  <div id="demo4">

      <h1>{{ firstname }}</h1>
      <h1>{{ lastname }}</h1>
      <h1>{{ fullname }}</h1>

      <h1 style="backgroup-color:gray;">
        Random No from computed property: {{ getrandomno }}
      </h1>
      <h1 style="backgroup-color:gray;">
        Random No from computed property: {{ getrandomno }}
      </h1>
      <h1 style="backgroup-color:gray;">
        Random No from computed property: {{ getrandomno }}
      </h1>
      <h1>Random No from method: {{ getrandomno1() }}</h1>
      <h1>Random No from method: {{ getrandomno1() }}</h1>
  </div>
</template>

<script>
export default {
  name: "Demo4",
  methods: {
    getrandomno1(){
      return Math.random();
    }
  },
  data() {
    return {
      firstname:"Krailasa",
      lastname:"Rattanachai"
    }
  },
  computed: {
    fullname(){
      return this.firstname + " " + this.lastname
    },
    getrandomno(){
      return Math.random();
    }
  }
};
</script>

<style lang=""></style>
