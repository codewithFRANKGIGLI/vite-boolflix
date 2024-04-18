<template>
    <div class="container d-flex flex-wrap justify-content-center gap-2 bg-dark p-5">
        <AppCard v-for="movie in store.moviesArray" :movieInfo="movie" :key="store.moviesArray.id"></AppCard>
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