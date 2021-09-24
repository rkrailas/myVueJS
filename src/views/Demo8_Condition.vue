<template>
    <div id="demo8">
        <div>
            <select v-model="type">
                <option value="A">A</option>
                <option value="B">B</option>
                <option value="C">C</option>
            </select>
        </div>
        <div v-if="type === 'A'">
            I am {{type}}
        </div>
        <div v-else-if="type === 'B'">
            I am {{type}}
        </div>
        <div v-else-if="type === 'C'">
            I am {{type}}
        </div>
        <div v-else>
            Not A/B/C
        </div>

        
    </div>
</template>
<script>
export default {
    name:"Demo8",
    data() {
        return {
            type: ""
        }
    },
}
</script>
<style>
    
</style>