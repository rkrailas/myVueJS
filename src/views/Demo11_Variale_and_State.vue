<template>
    <div id="Demo11">
        <div>{{ count }}</div>
        <div>{{ Math.random() }}</div>
        <div>Timestamp : {{ timestamp }}</div>
        <button @click="timestamp = Date.now()">Update Timestamp</button>
        <button @click="count++">Update Count</button>
    </div>
</template>
<script>
export default {
    created() {
        this.timestamp = 0;
    },
    mounted() {
        setInterval(()=> {
            //this.count++;
            console.log("Timestamp: " + this.timestamp)
        }, 100);
    },
    data() {
        return {
            count:0, //local State
        }
    },
}
</script>
<style>
    
</style>