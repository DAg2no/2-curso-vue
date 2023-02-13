<script setup>
/* defineProps(['title', 'id', 'body', 'colorText']) */

defineProps({
    title: {
        type: String,

    },
    id: {
        type: Number,

    },
    body: {
        type: String,
        default: 'no description',

    },
})

let emit = defineEmits(['cambiarfavoritonombre'])

</script>

<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">{{ id }} - {{ title }}</h5>
            <p>{{ body }}</p>
            <button @click="emit('cambiarfavorito', title)" class="btn btn-outline-danger">favorite</button>
        </div>
    </div>
</template>