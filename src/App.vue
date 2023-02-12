<script setup>
import ButtonCounter from './components/ButtonCounter.vue'
import blogPost from './components/BlogPost.vue'
import { ref } from 'vue';

const posts = ref([
    { title: 'post 1', id: 1, body: 'description 1' },
    { title: 'post 2', id: 2, body: 'description 2' },
    { title: 'post 3', id: 3, body: 'description 3' },
    { title: 'post 4', id: 4 },
])

let favorite = ref('')
let cambiarfavoritos = (title) => {
favorite.value = title;
}
</script>

<template>
    <div class="container pt-4">
        <h1>APP</h1>
        <h2>my favorite post {{ favorite }}</h2>
        <ButtonCounter />
        <ButtonCounter />

        <blogPost v-for="post in posts" :key="post.id" :title="post.title" :id="post.id" :body="post.body"  @cambiarfavoritos='cambiarfavoritos'/>
       
    </div>
</template>

