<template>
  <button id="special-for-you">
    <a href="#">{{ title }}</a>
  </button>
</template>

<script setup>
import {
  defineProps
} from 'vue'

defineProps({
  title: String
})
</script>

<style scoped>
#special-for-you {
  background: var(--secondary-color);
  padding: 30px 35px;
  border: none;
  border-radius: 10px;
  font-size: 38px;
  font-weight: normal;
  cursor: pointer;
  margin: 10px 0;
}

#special-for-you a {
  color: white;
}
</style>
