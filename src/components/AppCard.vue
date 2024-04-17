<template>
    <div class="card" style="width: 18rem;">
        <img src="" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{ movieInfo.title }}</h5>
            <p class="card-text"></p>
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item">Titolo Originale: {{ movieInfo.original_title }}</li>
            <li class="list-group-item">Lingua originale: {{ movieInfo.original_language }}</li>
            <li class="list-group-item">Voto medio: {{ movieInfo.vote_average }}</li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'AppCard',
        props: {
            movieInfo: Object
        },
    }
</script>

<style lang="scss" scoped>

</style>