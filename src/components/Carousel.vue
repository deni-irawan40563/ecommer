<template>
  <Carousel :itemsToShow="1" :wrap-around="true" :autoplay="5000">
    <Slide v-for="item in banner" :key="item.id">
      <img :src="item.img" class="banner">
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
import ProductCard from '../components/ProductCard.vue'

import 'vue3-carousel/dist/carousel.css';

const banner = ref([]);

onMounted(() => {
  axios.get(`http://localhost:2000/banner`)
    .then((res) => {
      banner.value = res.data;
    }).catch((err) => {
      console.log(err);
    });
});
</script>

<style scoped>
.banner {
  border-radius: 8px;
  width: 100%;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
