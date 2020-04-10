<template>
    <section class="about">
        <h2 class="section__title">Обо мне</h2>
        <div class="about-block">
            <div class="about-item">
                <img src="../assets/img/foto.jpg" alt="foto" class="about__img">
                <div class="connection">
                    <a href="#" class="connection__link"></a>
                    <a href="#" class="connection__link"></a>
                </div>
            </div>
            <div class="about-desc">
                <p class="about-desc__text">Привет. Меня зовут Олег, и я начинающий веб-разработчик. Мой стэк знаний состоит из HTML, CSS, JS, Jquery, PHP. В данный момент работаю в компании DD Planet на должности верстальщика. Также прохожу обучение на образовательном портале GeekBrains по профессии веб-разработчик.</p>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "About"
    }
</script>

<style lang="scss">

    @import "../assets/scss/_variable.scss";

    .about {
        min-height: 690px;
        @extend %center;
        padding: 60px 20px 100px;
    }
    .section__title {
        text-align: center;
        position: relative;
        text-transform: uppercase;
        &:after{
            position: absolute;
            bottom: 0;
            left: calc(50% - 110px);
            content: "";
            width: 220px;
            height: 6px;
            border-radius: 30px;
            background: #000;
        }
    }
    .about-block {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .about__img {
        display: block;
    }
    .connection {
        background: $orange;
        min-height: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .connection__link {
        width: 34px;
        height: 34px;
        border: 2px solid #fff;
        border-radius: 50%;
        margin: 0 20px;
        display: block;
        &:first-of-type{
            background: url("../assets/img/vk2.svg") center no-repeat;
            background-size: 24px;
        }
        &:nth-last-of-type(1){
            background: url("../assets/img/sent3.svg") center no-repeat;
            background-size: 24px;
        }
    }
    .about-desc {
        max-width: 700px;
    }

</style>