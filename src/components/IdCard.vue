<script setup>

// La variable firstName que es informada por el componente padre esta disponible inmediatamente en el <template>
defineProps({
  lastName: String,
  firstName: String,
  gender: String, // male or female
  height: Number,
  birth: Date,
  picture: String
})

// Aquí va todo el JavaScript
</script>

<template>
  <!-- Recomiendo empezar haciendo una pequeña parte estática -->
   <!-- Cuando veas que mas o menos se emieza a ver como quieres, empear a pasar propiedades -->
  <div class="container">
    <img :src="picture" alt="">
    <div>
        <p><strong>First name:</strong> {{ firstName }}</p>
        <p><strong>Last name:</strong> {{ lastName }}</p>
        <p><strong>Gender:</strong> {{ gender }}</p>
        <p><strong>Height:</strong> {{ height / 100 }}m</p>
        <p><strong>Birth:</strong> {{ birth.toDateString }}</p>
    </div>
  </div>
</template>

 <!-- El modificar scoped permite que todos los estilos definidos aquí se apliquen solamente al componente -->
<style scoped>
div > img {
    margin-right: 1rem;
}

div.container {
    display: flex;
    border: 2px solid #ccc;
    padding: 1rem;
}
</style>