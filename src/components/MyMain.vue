<template>
    <div class="container">

        <select name="" id="">
            <option value="alien">Alien</option>
        </select>
        <div class="card_container d_flex flex_wrap w_80_margin_auto pd_20">
            <MyCard v-for=" (element, index) in store.cardListArray" :key='index' :name="element.name"
                :image="element.card_images[0].image_url" :race="element.race"></MyCard>

        </div>

    </div>
</template>


<script>
import { store } from '../store.js'
import MyCard from './MyCard.vue';

export default {
    name: "MyMain",
    components: {
        MyCard
    },
    data() {
        return {
            store
        }
    }
}
</script>


<style scoped>
.container {
    background-color: #D28E3E;
    height: 100%;
    width: 100vw;
}

.card_container {
    background-color: white;
}
</style>