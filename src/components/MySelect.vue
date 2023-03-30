<template>
    <select name="" id="" @change="$emit('selected')" v-model="store.selectList">
        <option v-for="element in archetypeArray" :value="element">{{ element }}</option>
    </select>
</template>

<script>
import { store } from '../store.js';

export default {
    name: "MySelect",

    data() {
        return {
            store,

            archetypeArray: ["Human", "Alien", "Code Talker", "Anti"]
        }
    }
}

</script>


<style scoped>
select {
    position: relative;
    bottom: 20px;
    left: 190px;
    padding: 5px 15px;
    border-radius: 5px;
}
</style>