<template>
    <select name="" id="" @change="$emit('selected')" v-model="store.selectList">
        <option value=""></option>
        <option value="human">Human</option>
        <option value="alien">Alien</option>
        <option value="Code Talker">Code Talker</option>
        <option value="anti">anti</option>
        <option value="alien">Alien</option>
        <option value="alien">Alien</option>


    </select>
</template>

<script>
import { store } from '../store.js';

export default {
    name: "MySelect",

    data() {
        return {
            store
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