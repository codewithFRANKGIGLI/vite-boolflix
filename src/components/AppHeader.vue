<template>
    <div class="input-group mb-3">
        <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="button-addon2">
        <button class="btn btn-outline-secondary" type="button" id="button-addon2">Button</button>
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