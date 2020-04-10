<template>
    <section class="portfolio">
        <h2 class="section__title">Портфолио</h2>
        <div class="portfolio-block">
            <h3>Раздел находится в разработке</h3>
            <button class="btn">Подробнее</button>
        </div>

    </section>
</template>

<script>
    export default {
        name: "Portfolio"
    }
</script>

<style lang="scss">

    @import "../assets/scss/_variable.scss";

    .portfolio {
        padding: 40px 0;
        background: $gray-light;
        min-height: 500px;
    }
    .portfolio-block {
        @extend %center;
        text-align: center;
    }

</style>