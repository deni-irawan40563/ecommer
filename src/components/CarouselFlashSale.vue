<template>
  <Carousel :itemsToShow="4.5" :wrap-around="false" :breakpoints="breakpoints">
    <Slide v-for="product in flash" :key="product.id">
      <ProductCard :img="product.img" :name="product.name" :store="product.store" :price="product.price" :dicsPrice="product.discPrice" :rating="product.star" :disc="product.disc" />
    </Slide>
    <template #addons>
      <Navigation />
    </template>
  </Carousel>
</template>

<script setup>
import {
  Carousel,
  Navigation,
  Pagination,
  Slide
} from 'vue3-carousel';
import axios from 'axios';
import {
  onMounted,
  ref,
} from 'vue';
import ProductCard from '../components/ProductCardFlash.vue'
import 'vue3-carousel/dist/carousel.css';

const flash = ref([]);

onMounted(() => {
  axios.get(`http://localhost:2000/flashsale`)
    .then((res) => {
      flash.value = res.data;
    }).catch((err) => {
      console.log(err);
    });
});
</script>

<style scoped>
</style>
