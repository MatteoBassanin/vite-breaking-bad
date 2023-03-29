<template>
    <div>

        <MyCard v-for=" (element, index) in store.cardListArray" :key='index' :name="element.name"></MyCard>

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


<style scoped></style>