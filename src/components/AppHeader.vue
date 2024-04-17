<template>
    <div class="container p-2">
        <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Search series TV or movies">
            <button class="btn btn-warning" type="button" id="button-addon2">Search</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppHeader'
    }
</script>

<style lang="scss" scoped>
    @use '../assets/scss/partials/AppHeader.scss' as *;
</style>