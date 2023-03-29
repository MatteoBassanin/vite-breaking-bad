<template>
    <div class="big_card_wrapper">

        <div class="card_wrapper">
            <img :src="image" :alt="name">
        </div>
        <div class="text_description">
            <h5>{{ name }}</h5>

        </div>
    </div>
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


<style scoped>
.big_card_wrapper {
    width: calc(100% / 5)-20px;
    margin: 10px;
}

.card_wrapper,
.text_description {

    background-color: #D28E3E;

}


.text_description {
    text-align: center;
    padding: 0 50px;
}

img {

    width: 100%;
}
</style>