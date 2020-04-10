<template>
    <section class="contacts">
        <h2 class="section__title">Мои контакты</h2>
        <div class="contacts-block">
            <div class="connection">
                <a href="#" class="connection__link"></a>
                <a href="#" class="connection__link"></a>
            </div>
            <div class="phone">
                +7(902)901-77-94
            </div>
            <p class="contacts__text">Пишите. Звоните. Мы обязательно сработаемся :)</p>
        </div>

    </section>
</template>

<script>
    export default {
        name: "Contacts"
    }
</script>

<style lang="scss">

    @import "../assets/scss/_variable.scss";

    .contacts {
        padding: 40px 0;
        background: $gray-dark;
        .section__title {
            color: #fff;
            &:after{
                background: #fff;
            }
        }
    }
    .contacts-block {
        @extend %center;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: center;
        .connection {
            background: inherit;
            margin-bottom: 20px;
        }
        .phone {
            margin-bottom: 20px;
        }
    }
    .contacts__text {
        color: #fff;
    }

</style>