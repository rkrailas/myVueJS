<template>
    <div id="Demo12">
        <h1 ref="title">Waiting for change by Ref</h1>
        <input type="text" ref="input1" placeholder="This will be focused automatically">
    </div>
</template>
<script>
export default {
    mounted() {
        this.$refs["title"].textContent = "Krailas Rattanachai";
        this.$refs["input1"].focus();
        this.$refs["input1"].value = "1234";
    },
}
</script>
<style>
    
</style>