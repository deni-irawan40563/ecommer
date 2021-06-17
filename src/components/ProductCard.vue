<template>
  <div id="product-card">
    <div v-if="disc > 0" class="disc-label">{{ disc }}%</div>
    <img :src="img" :alt="name" loading='lazy' class="product-img" />
    <div v-if="rating === 1" class="product-rating">
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
    </div>
    <div v-else-if="rating === 2" class="product-rating">
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
    </div>
    <div v-else-if="rating === 3" class="product-rating">
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
    </div>
    <div v-else-if="rating === 4" class="product-rating">
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star grey"></i>
    </div>
    <div v-else-if="rating === 5" class="product-rating">
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
      <i class="fas fa-star yellow"></i>
    </div>
    <div v-else class="product-rating">
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
      <i class="fas fa-star grey"></i>
    </div>
    <h6>{{ store }}</h6>
    <p class="title">{{ name }}</p>
    <p v-if="disc > 0" class="discount"><s>{{ price }}</s></p>
    <h5 v-if="disc > 0">{{ dicsPrice }}</h5>
    <h5 v-if="disc === 0">{{ price }}</h5>
  </div>
</template>

<script setup>
import {
  defineProps
} from 'vue'

defineProps({
  img: String,
  name: String,
  store: String,
  disc: Number,
  price: String,
  dicsPrice: String,
  rating: Number
})
</script>

<style scoped>
#product-card {
  text-align: center;
  background: white;
  padding: 5px;
  border-radius: 10px;
  margin: 0 10px;
  cursor: pointer;
}

#product-card .product-img {
  width: 230px;
  height: 230px;
}

.disc-label {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  height: 45px;
  width: 45px;
  background-color: rgb(231, 80, 80);
  border-radius: 50%;
  font-size: 12px;
  position: absolute;
  right: 0;
  font-weight: bold;
}

.yellow {
  color: orange;
}

.grey {
  color: gainsboro;
}

.title {
  font-size: 14px;
}

.discount {
  color: red;
  font-size: 12px;
}
</style>
