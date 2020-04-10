<template>
    <div class="skills-block">
        <div class="skills-slider" :style="{'margin-left': '-' + (100 * currentSlideIndex) + '%'}">
            <CarouselItem
                v-for="item in carousel_data"
                :key="item.id"
                :item_data="item"
            />
        </div>
        <div class="skills-controls">
            <button @click="prevSlide" class="prev"></button>
            <button @click="nextSlide" class="next"></button>
        </div>

    </div>
</template>

<script>

    import CarouselItem from "./CarouselItem";

    export default {
        name: "Carousel",
        props: {
            carousel_data: {
                type: Array,
                default: () => []
            },
            interval: {
                type: Number,
                default: 0
            }
        },
        data(){
            return {
                currentSlideIndex: 0,
                autoSlide: 0,
                limit: Math.ceil(this.carousel_data.length / 3)
            }
        },
        components: {
            CarouselItem
        },
        methods: {
            prevSlide(){
                clearInterval(this.autoSlide);
                if(this.currentSlideIndex > 0){
                    this.currentSlideIndex--;
                }else {
                    this.currentSlideIndex = this.limit - 1;
                }
            },
            nextSlide(){
                clearInterval(this.autoSlide);
                if(this.currentSlideIndex >= this.limit - 1){
                    this.currentSlideIndex = 0;
                }else {
                    this.currentSlideIndex++;
                }
            },
            startSlide(){
                if(this.currentSlideIndex >= this.limit - 1){
                    this.currentSlideIndex = 0;
                }else {
                    this.currentSlideIndex++;
                }
            }

        },
        mounted() {
            if(this.interval > 0){
                let vm = this;
                this.autoSlide = setInterval( function(){
                    vm.startSlide()
                }, vm.interval)
            }
        }
    }
</script>

<style lang="scss">
    .skills-block {
        max-width: 1620px;
        margin: 0 auto;
        overflow: hidden;
        text-align: center;
    }
    .skills-slider {
        display: flex;
        align-items: center;
        transition: all ease .5s;
        margin-bottom: 20px;
    }
    .skills-controls {
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
    .prev,
    .next {
        cursor: pointer;
        outline: none;
        border: none;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: #fff;
        background-position: center;
        background-repeat: no-repeat;
        background-size: 20px;
    }
    .prev {
        background-image: url("../../assets/img/prev.svg");
    }
    .next {
        background-image: url("../../assets/img/next.svg");
    }
</style>