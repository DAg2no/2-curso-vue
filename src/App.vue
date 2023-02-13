<script setup>
import ButtonCounter from './components/ButtonCounter.vue'
import blogPost from './components/BlogPost.vue'
import { ref } from 'vue';

const posts = ref([])

let favorite = ref('')

let cambiarfavorito = (title) => {
    favorite.value = title;
}
fetch('https://jsonplaceholder.typicode.com/posts')
    .then(res => res.json())
    .then(data => posts.value = data)
</script>

<template>
    <div class="container pt-4">
        <h1>APP</h1>
        <h2>my favorite post {{ favorite }}</h2>
        <ButtonCounter />
        <ButtonCounter />

        <blogPost v-for="post in posts" :key="post.id" :title="post.title" :id="post.id" :body="post.body"
            :cambiarfavorito="cambiarfavorito" />

    </div>
</template>

