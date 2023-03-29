<template>
  <MyLoading></MyLoading>
  <MyHeader></MyHeader>
  <MyMain></MyMain>
</template>



<script>
import axios from 'axios';

import { store } from './store.js';

import MyLoading from './components/MyLoading.vue';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyCard from './components/MyCard.vue';

export default {
  components: {
    MyHeader,
    MyMain,
    MyCard,
    MyLoading
  },
  data() {
    return {
      store
    }
  },
  created() {

    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?staple=yes')
      .then(response => {
        this.store.cardListArray = response.data.data;
        this.store.loading = false;
        console.log(response)
      }
      )
  }
}
</script>



<style></style>