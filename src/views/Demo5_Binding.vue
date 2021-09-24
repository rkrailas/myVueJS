<template>
  <div id="demo5">
    <img v-bind:src="imageUrl" v-bind:height="myheight" />
    <div>
      <a v-bind:href="myurl">My Website</a>
      <br><a :href="myurl">My Website</a>
    </div>
    <div :class="[flase ? error : important]">CodeMobiles</div>
    <div :style="{color:myColor, fontSize:myfontSize}">Binding Style</div>
    <div :style="isActive ? styleObj : ''">Binding Style Object</div>
    <button @click="isActive = !isActive">Toggle Button</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageUrl:
        "https://images.unsplash.com/photo-1632418128534-06a848984ab5?ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw4fHx8ZW58MHx8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
      myheight: 300,
      myurl:"http://www.google.com",
      error: "error_class",
      important: "important_class",
      myColor: "red",
      myfontSize: "50px",
      styleObj: {
          backgroundColor: 'yellow',
          colot: 'green'
      },
      isActive: false,
    };
  },
};
</script>

<style>
    .error_class {
        background-color: red;
        color:white;
    }
    .important_class{
        font-weight: 900;
    }
</style>
