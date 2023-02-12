<script setup>
import ButtonCounter from './components/ButtonCounter.vue'
import blogPost from './components/BlogPost.vue'

</script>

<template>
    <div class="container pt-4">
        <h1>APP</h1>
<ButtonCounter />
<ButtonCounter />

<blogPost title="Post 1"/>
<blogPost title="Post 2"/>
<blogPost title="Post 3"/>

    </div>
</template>

