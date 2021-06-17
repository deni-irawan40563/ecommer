<template>
  <div id="section-title">
    <div class="line" />
    <h2>{{ title }}</h2>
    <div class="line" />
  </div>
</template>

<script setup>
import {
  defineProps
} from 'vue'

defineProps({
  title: String,
  line: Boolean,
})
</script>

<style scoped>
#section-title {
  padding-top: 20px;
  display: grid;
  grid-template-columns: 2fr 1fr 2fr;
  text-align: center;
  width: var(--container-size);
  margin: 0 auto;
  color: #0f0f0f;
}

.line {
  height: 2px;
  border-bottom: 2px solid grey;
  background: black;
}
</style>
