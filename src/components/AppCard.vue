<template>
    <div class="card text-white" style="width: 18rem;">
        <img :src="'https://image.tmdb.org/t/p/w342'+ movieInfo.poster_path" class="card-img" alt="...">
        <div class="hoverOp card-img-overlay">
            <h5 class="card-title">{{ movieInfo.title }}</h5>
            <p class="card-text">Titolo Originale: {{ movieInfo.original_title }}</p>
            <p class="card-text">Lingua originale: {{ movieInfo.original_language }}</p>
            <p class="card-text">Voto medio: {{ movieInfo.vote_average }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppCard',
        props: {
            movieInfo: Object
        }
    }
</script>

<style lang="scss" scoped>
    .hoverOp {
        opacity: 0;
        &:hover {
            opacity: 1;
            transition: 1s;
        }
    }
</style>