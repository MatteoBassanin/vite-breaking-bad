<template>
    <div class="container">
        <MySelect @selected="prova"></MySelect>
        <!-- <select name="" id="">
            <option value="alien">Alien</option>

        </select> -->
        <div class="w_80_margin_auto big_wrapper">
            <BannerCounter></BannerCounter>
            <!-- <div class="black_banner ">
                <span>Found 64 cards</span>
            </div> -->
            <div class="card_container d_flex flex_wrap ">
                <MyCard v-for=" (element, index) in store.cardListArray" :key='index' :name="element.name"
                    :image="element.card_images[0].image_url" :race="element.race"></MyCard>

            </div>

        </div>

    </div>
</template>


<script>
import { store } from '../store.js'
import MyCard from './MyCard.vue';
import BannerCounter from './BannerCounter.vue';
import MySelect from './MySelect.vue';

export default {
    name: "MyMain",
    components: {
        MyCard,
        BannerCounter,
        MySelect
    },
    data() {
        return {
            store
        }
    },
    methods: {
        prova() {
            alert("ciao")
        }
    }
}
</script>


<style scoped>
.container {
    background-color: #D28E3E;
    height: 100%;
    width: 100vw;
    padding: 40px;
}

.big_wrapper {
    background-color: white;
    padding: 50px;
}


/* 
select {
    position: relative;
    bottom: 20px;
    left: 190px;
    padding: 5px 15px;
    border-radius: 5px;
} */

/* .black_banner {
    height: 80px;
    color: white;
    background-color: #212529;
    line-height: 80px;
    padding: 0 40px;
    margin: 0 10px;

} */
</style>