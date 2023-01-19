<script>
export default {
    name: 'AppHero',
    data() {
        return {
            images: ['guernica.jpg', 'notte-stellata.jpg']
        }
    },
    methods: {
        createImg(image) {
            const url = new URL(`../assets/${image}`, import.meta.url);
            return url.href;
        }
    }
}
</script>

<template>
    <div v-for="image in images">
        <img :src="createImg(image)" alt="banner">
    </div>
</template>

<style>
img {
    width: 100%;
}
</style>