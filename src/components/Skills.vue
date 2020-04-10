<template>
    <section class="skills">
        <h2 class="section__title">Навыки</h2>
            <Carousel
                :carousel_data="sliderItems"
                :interval = "5000"
            />
    </section>
</template>

<script>

    import Carousel from "./elements/Carousel";

    export default {
        name: "Skills",
        components: {
            Carousel
        },
        data(){
            return {
                sliderItems: [
                    {id:1, name: 'img1',img: 'web.jpg'},
                    {id:2, name: 'img2',img: 'git.jpg'},
                    {id:3, name: 'img3',img: 'html.jpg'},
                    {id:4, name: 'img4',img: 'css.jpg'},
                    {id:5, name: 'img5',img: 'js1.jpg'},
                    {id:6, name: 'img6',img: 'js2.jpg'},
                    {id:7, name: 'img7',img: 'php1.jpg'},
                    {id:8, name: 'img8',img: 'php2.jpg'},
                ]
            }
        }
    }
</script>

<style lang="scss">

    @import "../assets/scss/_variable.scss";

    .skills {
        padding: 40px 0;
        background: $gray-dark;
        .section__title {
            color: #fff;
            &:after{
                background: #fff;
            }
        }
    }

</style>