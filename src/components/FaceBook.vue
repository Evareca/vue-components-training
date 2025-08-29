<script setup>
defineProps({
  firstName: String,
  lastName: String,
  country: String,
  img: String,
  isStudent: Boolean
});
</script>

<template>
  <div class="card">
    <img :src="img" alt="" />
    <div>
      <p><strong>First name:</strong> {{ firstName }}</p>
      <p><strong>Last name:</strong> {{ lastName }}</p>
      <p><strong>Country:</strong> {{ country }}</p>
      <p><strong>Type:</strong> {{ isStudent ? 'Student' : 'Teacher' }}</p>
    </div>
  </div>
</template>

<style scoped>
</style>