<template>
  <div>
    <h1>Data</h1>
    <button
      @click="
        count++;
        isLogged = true;
      "
    >
      Count++
    </button>
    <span>{{ count }}</span>
    <div>{{ message }}</div>
    <div>{{ isLogged }}</div>
    <input type="text" placeholder="Enter some message" v-model="message" />
    <h2 v-if="isLogged">Yahooo</h2>
    <div>{{ account }}</div>
    <div class="content">{{ courses }}</div>
    <ul>
        <li v-for="(item, index) in courses" :key="index">{{index}} . {{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo3",
  mounted() {
    this.message = "Nong Nine";
  },
  data() {
    return {
      count: 0,
      message: "",
      isLogged: false,
      account: {
        user: "admin",
        password: "1234",
      },
      courses: ["Lesson1", "lesson2", "lesson3", "lesson4"],
    };
  },
};
</script>

<style>
</style>
