<template>
    <div class="container p-2">
        <div class="input-group mb-3">
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