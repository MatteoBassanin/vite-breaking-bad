<template>
    <div class="container">
        <!-- <MySelect @selected="getInfoData"></MySelect> -->

        <div class="w_80_margin_auto big_wrapper">
            <BannerCounter></BannerCounter>

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
            console.log(store.selectList)
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
</style>