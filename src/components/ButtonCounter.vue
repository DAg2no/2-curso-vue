<script setup>
import { ref } from 'vue';

let counter = ref(0)
let increment = () => counter.value ++


</script>

<template>
    <button @click="increment">counter {{ counter }}</button>
</template>