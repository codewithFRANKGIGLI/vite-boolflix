<template>
    <AppHeader @searchClick="getMoviesFromApi(), getSeriesFromApi()"></AppHeader>
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
            getMoviesFromApi() {
                const queryParams = {
                    api_key:'612e3f2fe173487edf095e3b2629965d',
                };
                if (store.inputSearch !== '') {
                    queryParams.query = store.inputSearch;
                }
                axios.get('https://api.themoviedb.org/3/search/movie',{
                    params: queryParams
                })
                
                .then((response) => {
                    this.store.moviesArray = response.data.results;
                })
            },
            getSeriesFromApi() {
                const queryParams = {
                    api_key:'612e3f2fe173487edf095e3b2629965d',
                };
                if (store.inputSearch !== '') {
                    queryParams.query = store.inputSearch;
                }
                axios.get('https://api.themoviedb.org/3/search/tv',{
                    params: queryParams
                })
                
                .then((response) => {
                    this.store.seriesArray = response.data.results;
                })
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>