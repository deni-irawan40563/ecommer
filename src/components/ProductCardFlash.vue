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
    <div class="price-section">
      <p class="discount"><s>{{ price }}</s></p>
      <h5>{{ dicsPrice }}</h5>
    </div>
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
  text-align: left;
  background: white;
  padding: 5px 15px;
  border-radius: 20px;
  cursor: pointer;
}

#product-card .product-img {
  width: 200px;
  height: 200px;
}

#product-card h6 {
  padding: 3px;
  background: var(--primary-color);
  color: white;
  width: 60%;
  font-size: 10px;
  text-align: center;
  border-radius: 3px;
}

.price-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.price-section h5 {
  color: red;
  font-size: 1em;
}

.yellow {
  color: orange;
}

.grey {
  color: gainsboro;
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
  margin-right: 20px;
}

.title {
  font-size: 13px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 200px;
}

.discount {
  font-size: 12px;
}
</style>
