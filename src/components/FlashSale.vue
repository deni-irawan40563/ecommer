<template>
  <div id="flash-sale">
    <div class="container">
      <div class="flash-title">
        <p class="plus1">+</p>
        <p>FLASH<br />SALE</p>
        <div class="plus-container">
          <p class="plus2">+</p>
          <p class="flash-sub-title">Lebaran Spesial</p>
        </div>
        <p class="plus3">+</p>
      </div>
      <div class="carousel">
        <CarouselFlashSale />
      </div>
    </div>
  </div>
</template>

<script setup>
import CarouselFlashSale from '../components/CarouselFlashSale.vue'
</script>

<style>
#flash-sale {
  background: var(--secondary-color);
  margin: 0 0 10px 0;
}

.container {
  width: var(--container-size);
  margin: 0 auto;
  padding: 5px;
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 20px;
}

.flash-title {
  color: white;
  width: 230px;
}

.flash-title p {
  font-size: 60px;
  text-shadow: 3px 3px var(--primary-color);
  font-weight: bold;
}

.flash-title .flash-sub-title {
  text-align: center;
  background: #0AAC7D;
  padding: 5px 10px;
  color: white;
  text-shadow: none;
  font-size: 12px;
  width: 150px;
  border-radius: 3px;
}

.flash-title .plus1 {
  text-align: right;
  font-size: 16px;
}

.plus-container {
  display: grid;
  grid-template-columns: 1fr 3fr;
  margin-left: -80px;
}

.plus-container .plus2 {
  display: flex;
  align-items: center;
  height: 20px;
  font-size: 40px;
}

.flash-title .plus3 {
  text-align: right;
}

.carousel {
  height: auto;
  background: rgba(255, 255, 255, 0.4);
}
</style>
