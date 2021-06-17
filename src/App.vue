<template>
  <Header />
  <Navbar />
  <Menu />
  <div class="carousel">
    <CarouselComp />
  </div>
  <div class="benefit-section">
    <Bennefit />
  </div>
  <FlashSale />
  <p class="exclusive-title">NATURAL FARM <b>EXCLUSIVE</b></p>
  <main class="main-section">
    <Carousel :itemsToShow="5" snapAlign="start">
      <Slide v-for="product in exclusive" :key="product.id">
        <ProductCard :img="product.img" :name="product.name" :store="product.store" :price="product.price" :dicsPrice="product.discPrice" :rating="product.star" :disc="product.disc" />
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </main>
  <SectionTitle title="BEST SELLER" />
  <main class="main-section">
    <Carousel :itemsToShow="5" snapAlign="start">
      <Slide v-for="product in bests" :key="product.id">
        <ProductCard :img="product.img" :name="product.name" :store="product.store" :price="product.price" :dicsPrice="product.discPrice" :rating="product.star" :disc="product.disc" />
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </main>
  <SectionTitle title="NEW PRODUCT" />
  <main class="main-section">
    <Carousel :itemsToShow="5" snapAlign="start">
      <Slide v-for="product in newsProducts" :key="product.id">
        <ProductCard :img="product.img" :name="product.name" :store="product.store" :price="product.price" :dicsPrice="product.discPrice" :rating="product.star" :disc="product.disc" />
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </main>
  <SectionTitle title="FEATURED" />
  <main class="main-section">
    <Carousel :itemsToShow="5" snapAlign="start">
      <Slide v-for="product in featureds" :key="product.id">
        <ProductCard :img="product.img" :name="product.name" :store="product.store" :price="product.price" :dicsPrice="product.discPrice" :rating="product.star" :disc="product.disc" />
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
  </main>
  <SectionTitle title="Special for you!" />
  <div class="special-for-you">
    <SpecialForYou title="Natural Farm Express" />
    <SpecialForYou title="Natural Farm Tips & Info" />
    <SpecialForYou title="Natural Farm Store Location & Number" />
  </div>
  <EmailSub />
  <div class="footer">
    <Footer />
  </div>
</template>

<script setup>
import axios from 'axios';
import {
  onMounted,
  ref,
} from 'vue';
import {
  Carousel,
  Navigation,
  Pagination,
  Slide
} from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';
import Header from './components/Header.vue'
import Navbar from './components/Navbar.vue'
import Menu from './components/Menu.vue'
import Bennefit from './components/Bennefit.vue'
import ProductCard from './components/ProductCard.vue'
import SectionTitle from './components/SectionTitle.vue'
import EmailSub from './components/EmailSub.vue'
import Footer from './components/Footer.vue'
import CarouselComp from './components/Carousel.vue'
import FlashSale from './components/FlashSale.vue'
import SpecialForYou from './components/SpecialForYou.vue'

const bests = ref([]);
const newsProducts = ref([]);
const featureds = ref([]);
const exclusive = ref([]);

onMounted(() => {
  axios.all([
      axios.get('http://localhost:2000/bestSeller'),
      axios.get('http://localhost:2000/newProduct'),
      axios.get('http://localhost:2000/featured'),
      axios.get('http://localhost:2000/exclusive')
    ])
    .then(axios.spread(function (response1, response2, response3, response4) {
      bests.value = response1.data;
      newsProducts.value = response2.data;
      featureds.value = response3.data
      exclusive.value = response4.data
    }))
    .catch(function (error) {
      alert(error)
    });
});
</script>

<style scoped>
.main-section {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  width: var(--container-size);
  margin: 0 auto;
}

.carousel {
  width: 99%;
  margin: 0 auto;
}

.special-for-you {
  margin: 0 auto;
  width: var(--container-size);
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 50px;
  padding-top: 20px;
}

.benefit-section {
  background: ghostwhite;
  padding: 10px 0;
}

.exclusive-title {
  color: #0f0f0f;
  text-align: center;
  font-size: 25px;
  margin-top: 20px;
}

@media (max-width: 720px) {
  .special-for-you {
    display: block;
  }
}
</style>
