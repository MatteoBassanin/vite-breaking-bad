<template>
    <select name="" id="" @change="$emit('selected')">
        <option value="alien">Alien</option>
        <option value="human">Human</option>
        <option value="alien">Alien</option>
        <option value="alien">Alien</option>
        <option value="alien">Alien</option>
        <option value="alien">Alien</option>
        <option value="alien">Alien</option>


    </select>
</template>

<script>
export default {
    name: "MySelect"
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