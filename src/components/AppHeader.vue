<template>
    <div class="container d-flex p-2 justify-content-between bg-dark p-3">
        <div>
            <h1 class="text-danger ">BOOLFLIX</h1>
        </div>
        <div class="input-group w-50 mb-3">
            <input v-model="store.inputSearch" type="text" class="form-control" placeholder="Search series TV or movies">
            <button @click="$emit('searchClick')" class="btn btn-warning" type="button" id="button-addon2">Search</button>
        </div>
    </div>
</template>

<script>
    import { store } from '../store';
    export default {
        name: 'AppHeader',
        data() {
            return {
                store
            }
        }
    }
</script>

<style lang="scss" scoped>
    @use '../assets/scss/partials/AppHeader.scss' as *;
</style>