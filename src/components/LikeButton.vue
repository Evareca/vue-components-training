<script setup>
import { computed, ref } from 'vue';


const colors = ['red', 'green', 'blue', '#125467', 'rgb(233,11,44)']

// 1. Primero ver si tu variable de estado se comporta como esperas cambiando su valor inicial 
const likes = ref(0)
// Con funcion de callback: añadimos aqui const incrementLikes = () => likes.value++ y en template lo sustituimos por <button :style="{backgroundColor: 'purple'}" v-on:click="incrementLikes">{{ likes }} Likes</button>
// v-on:click y @click es lo mismo

const buttonColor = computed(()=> {
    return colors[likes.value % colors.length]
})

</script>

<template>
<button :style="{backgroundColor: colors[likes % colors.length]}" v-on:click="likes++">{{ likes }} Likes</button>
</template>

<style scoped>
button {
    cursor: pointer;
}
</style>