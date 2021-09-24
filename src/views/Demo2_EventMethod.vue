<template>
  <div app="demo2">
    <h1>Event and Method</h1>
    <button v-on:click="clickMe">clickMe</button>
    <button v-on:click="clickMe2('Welcome to VueJS')">clickMe2</button>
    <button @click="clickMe3('Welcome to VueJS 33333')">clickMe3</button>
    <h3>{{ getTimestamp() }}</h3>
  </div>
</template>

<script>
export default {
  name: "Demo2",
  mounted() {
    this.initial();
  },
  methods: {
    initial() {
      console.log("Initialization")
    },
    clickMe() {
      alert("Hi");
    },
    clickMe2(message) {
      alert(message);
    },
    clickMe3(message) {
      alert(message);
    },
    getTimestamp() {
      return Date();
    },
  },
};
</script>

<style>
button {
  margin-right: 8px;
}
</style>
