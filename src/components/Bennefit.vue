<template>
  <div class="container">
    <button><img src="../assets/icons/100.svg" /> 100% Original Product</button>
    <button><img src="../assets/icons/freeshipping.svg" /> Free Shipping</button>
    <button><img src="../assets/icons/discount.svg" /> Discount VIP Member</button>
  </div>
</template>

<script>
</script>

<style scoped>
.container {
  margin: 0 auto;
  width: var(--container-size);
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 30px;
}

.container button {
  padding: 10px;
  background: var(--secondary-color);
  border: none;
  color: white;
  border-radius: 5px;
  font-size: 14px;
}

.container button img {
  height: 20px;
}
</style>
