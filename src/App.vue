<template>
    <AppHeader></AppHeader>
    <AppMain></AppMain>
</template>

<script>
    import { store } from "./store.js";
    import AppHeader from './components/AppHeader.vue';
    import AppMain from './components/AppMain.vue';
    import axios from 'axios';

    export default {
        components: {
            AppHeader,
            AppMain
        },
        data() {
            return {
                store,
            }
        },
        methods: {
            getDataMoviesFromApi() {
                axios.get('https://api.themoviedb.org/3/search/movie?api_key=612e3f2fe173487edf095e3b2629965d')
                .then((response) => {
                    
                })
            }
        },
        
    }
</script>

<style lang="scss" scoped>

</style>