<template>
    <div id="demo10">
        <h1>Lifecycle Hooks</h1>
        <div>{{myCount}}</div>
        <br><button @click="addMyCount">Change ++</button>
    </div>
</template>
<script>
export default {
    name: "Demo10",
    methods: {
        addMyCount(){
            this.myCount ++;
        }
    },
    data() {
        return {
            myCount:0,
        }
    },
    beforeCreate() {
        console.log("beforeCreate");
    },
    created() {
        console.log("created");
    },
    beforeMount() {
        console.log("beforeMount");
    },
    mounted() {
        console.log("mounted");
    },
    beforeUpdate() {
        console.log("beforeUpdate");
    },
    updated() {
        console.log("updated");
    },
}
</script>
<style>
    
</style>