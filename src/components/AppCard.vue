<template>
    <div class="card text-white" style="width: 20rem;">
        <img :src="'https://image.tmdb.org/t/p/w342'+ movieInfo.poster_path" class="card-img" alt="...">
        <div class="hoverOp card-img-overlay">
            <h5 class="card-title">{{ movieInfo.title }}</h5>
            <p class="card-text">Titolo Originale: {{ movieInfo.original_title }}</p>
            <p class="card-text">Lingua originale:
                <img class="w-25 m-2" :src="getImageUrl(movieInfo.original_language)" alt="">
            </p>
            <p class="card-text">Voto medio: {{ movieInfo.vote_average }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppCard',
        props: {
            movieInfo: Object
        },
        methods: {
            getImageUrl(name) {
                return new URL(`../assets/img/flags/${name}.png`, import.meta.url).href;
            },
        },
    }
</script>

<style lang="scss" scoped>
    .hoverOp {
        opacity: 0;
        &:hover {
            opacity: 1;
            transition: 1s;
        }
    };
    h5, p {
        text-shadow: 1px 1px 1px black;
    }
</style>