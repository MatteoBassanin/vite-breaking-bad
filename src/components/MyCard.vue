<template>
    <div class="big_card_wrapper">

        <div class="card_wrapper">
            <img :src="image" :alt="name">
        </div>
        <div class="text_description">
            <h5>{{ name }}</h5>
            <h6>{{ race }}</h6>
        </div>
    </div>
</template>

<script>

export default {
    name: "MyCard",
    props: {
        name: String,
        image: String,
        race: String,
    }
}
</script>


<style scoped>
.big_card_wrapper {
    width: calc(100% / 5 - 20px);
    margin: 10px;
}

.card_wrapper,
.text_description {
    font-size: 30px;
    background-color: #D28E3E;
    padding: 0 0 30px 0;
    width: 100%;
    min-height: 150px;

}


.text_description {
    text-align: center;

}

img {

    width: 100%;
}

h5 {
    color: white;
    margin-bottom: 30px;
}
</style>