<script>
import { store } from './store';
import axios from 'axios';

// IMPORTIAMO LE APP 

import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppCard from './components/AppCard.vue';



export default {
  data() {
    return {

    };
  },

  // COMPONENTS

  components: { AppHeader, AppMain, AppCard, AppFooter },
  created() {
    axios.get(`${store.apiUri}/products`).then((res) => {
      this.products = res.data;
    });
  }
};



</script>



<template>
  <AppHeader></AppHeader>
  <div v-for="product in products"> {{ product.name }}</div>
  <AppMain></AppMain>


  <AppFooter></AppFooter>
</template>




<style lang ="scss">
@use'./styles/general.scss';
</style>

