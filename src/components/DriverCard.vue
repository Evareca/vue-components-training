<script setup>

import { computed } from 'vue';

const props = defineProps({
  name: String,
  rating: Number,
  picture: String,
  car: Object
})

const stars = '★'.repeat(Math.round(props.rating)) + '☆'.repeat(5 - Math.round(props.rating))

</script>

<template>
  <div class="container">
    <img :src="picture" alt="">
    <div>
        <p> {{ stars }}</p>
        <p><strong>Name:</strong> {{ name }}</p>
        <p><strong>Rating:</strong> {{ rating }}</p>
    </div>
  </div>
</template>

<style scoped>
</style>