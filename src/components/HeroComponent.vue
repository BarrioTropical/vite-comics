<template>
    <div class="hero">
    </div>
</template>

<script>
    export default {
        name: 'HeroComponent',
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/generals.scss' as *;


    .hero{
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;
        height: 400px;
    }
</style>