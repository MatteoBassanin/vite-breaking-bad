<template>
  <MyLoading></MyLoading>
  <MyHeader></MyHeader>
  <MySelect @selected="getInfoData"></MySelect>
  <MyMain></MyMain>
</template>



<script>
import axios from 'axios';

import { store } from './store.js';


import MySelect from './components/MySelect.vue';
import MyLoading from './components/MyLoading.vue';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import MyCard from './components/MyCard.vue';

export default {
  components: {
    MyHeader,
    MyMain,
    MyCard,
    MyLoading,
    MySelect
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getInfoData() {

      let searchApi = "https://db.ygoprodeck.com/api/v7/cardinfo.php?staple=yes"

      if (store.selectList.length > 0) {
        searchApi += `&archetype=${store.selectList}`;
      }
      axios.get(searchApi)
        .then(response => {
          this.store.cardListArray = response.data.data;
          this.store.loading = false;
          console.log(response)
        }
        );
    }
  },
  created() {
    this.getInfoData();
  },

}
</script>



<style></style>