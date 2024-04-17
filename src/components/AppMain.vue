<template>
    <div class="container">
        <AppCard v-for="movie in store.moviesArray"></AppCard>
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