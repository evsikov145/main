<template>
    <div class="skills-slider__item">
        <img v-bind:src=" require('@/assets/img/certificate/' + item_data.img)" alt="certificate">
    </div>
</template>

<script>
    export default {
        name: "CarouselItem",
        props: {
            item_data: {
                type: Object,
                default: () => {}
            }
        }
    }
</script>

<style lang="scss">
.skills-slider__item {
    img{
        margin: 0 20px;
        width: 500px;
    }
}
</style>