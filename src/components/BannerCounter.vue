<template>
    <div class="black_banner ">
        <span>{{ cardsFounded }}</span>
    </div>
</template>

<script>
import { store } from '../store.js';

export default {
    name: "BannerCounter",
    data() {
        return {
            store,


        }
    },
    computed: {
        cardsFounded() {
            return `Found ${this.store.cardListArray.length} cards`
        }
    }
}
</script>


<style scoped>
.black_banner {
    height: 80px;
    color: white;
    background-color: #212529;
    line-height: 80px;
    padding: 0 40px;
    margin: 0 10px;

}
</style>