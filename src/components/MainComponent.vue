<template>
    <main>
    <section class="content">
    <h3 class="container">-- Content goes her --</h3>
    </section>

    <section class="merch">
        <ul class="container">
        <li>
        <div>
            <img src="../assets/img/buy-comics-digital-comics.png" alt="">
            <h3>Digital Comics</h3>
        </div>
        
        </li>
        </ul>
    </section>

    </main>
</template>

<script>
    export default {
        name: 'MainComponent',
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables' as *;
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/generals.scss' as *;

    .content{
        background-color: $greydark;
        color: $white;
    }

    .merch{
        background-color: $blue;
        color: $white;
    }
    img{
        max-width: 50px;
    }

    section{
        padding: 20px;
    }
</style>