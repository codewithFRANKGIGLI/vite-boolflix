<template>
    <div class="container bg-dark p-5">
        <div class="row text-white">
            <div class="col-6">
                <h1>Movies</h1>
            </div>
            <div class="col-6">
                <h1>Series TV</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-6 d-flex flex-wrap gap-3">
                <AppCard v-for="movie in store.moviesArray" :movieInfo="movie" :key="store.moviesArray.id"></AppCard>
            </div>
            <div class="col-6 d-flex flex-wrap gap-3">
                <AppCard v-for="series in store.seriesArray" :movieInfo="series" :key="store.seriesArray.id"></AppCard>
            </div>
        </div>
    </div>
</template>

<script>
    import { store } from '../store.js';
    import AppCard from './AppCard.vue';
    export default {
        name: 'AppMain',
        components: {
            AppCard
        },
        data() {
            return {
                store
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>