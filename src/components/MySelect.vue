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
    top: 33px;
    right: 30px;
    padding: 5px 15px;
    border-radius: 5px;
}
</style>