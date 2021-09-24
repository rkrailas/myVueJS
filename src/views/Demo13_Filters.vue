<template>
    <div id="Demo13">
        <h2>{{ reverseArray }}</h2>
    </div>
</template>
<script>
export default {
    name: "Demo13",
    data() {
        return {
            myValue:[1,2,3]
        }
    },
    computed: {
      reverseArray() {
        return this.myValue.slice().reverse();
      }
    }
}
</script>
<style>
    
</style>