<template>
    <div class="card text-white lh-lg myTextShadow" style="width: 18rem; height: 27rem;">
        <img :src="'https://image.tmdb.org/t/p/w342'+ movieInfo.poster_path" class="card-img" alt="">
        <div class="hoverOp card-img-overlay">
            <h5 class="fs-5 card-title">{{ movieInfo.title || movieInfo.name }}</h5>
            <p class="card-text">Titolo Originale: {{ movieInfo.original_title || movieInfo.original_name }}</p>
            <p class="card-text">Lingua originale:
                <img class="w-25 m-2" :src="getImageUrl(movieInfo.original_language)" alt="">
            </p>
            <div class="card-text">Voto medio:
                <i v-show="Math.ceil(movieInfo.vote_average / 2)>=1" class="fa-solid fa-star"></i>
                <i v-show="Math.ceil(movieInfo.vote_average / 2)>=2"class="fa-solid fa-star"></i>
                <i v-show="Math.ceil(movieInfo.vote_average / 2)>=3"class="fa-solid fa-star"></i>
                <i v-show="Math.ceil(movieInfo.vote_average / 2)>=4"class="fa-solid fa-star"></i>
                <i v-show="Math.ceil(movieInfo.vote_average / 2)>=5"class="fa-solid fa-star"></i>
            </div>
            <div class="card-text">
                <p class="lh-1 m-0">Overview:</p>
                <div class="lh-1">{{ movieInfo.overview }}</div>
            </div>
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
            }
        },
    }
</script>

<style lang="scss" scoped>
    ::-webkit-scrollbar {
        width: 1px;
    }
    .hoverOp {
        opacity: 0;
        &:hover {
            opacity: 1;
            transition: 1s;
            background-color: rgba($color: #000000, $alpha: 0.5);
        }
    };
    .myTextShadow {
        text-shadow: 1px 1px 1px red;
    };
    i {
        color: yellow;
    }
    
</style>