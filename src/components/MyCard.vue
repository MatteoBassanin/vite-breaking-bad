<template>
    <div>{{ name }}</div>
    <img :src="image" alt="">
</template>

<script>

export default {
    name: "MyCard",
    props: {
        name: String,
        image: String,
    }
}
</script>


<style scoped></style>