<template>
    <header class="header">
        <div class="header-main">
            <div class="header-block">
                <h1 class="header__title">Евсиков Олег</h1>
                <h3 class="header__subtitle">Junior web developer</h3>
                <button class="btn btn--orange">Заказать работу</button>
            </div>
            <div class="header-optionally">
                <div class="phone">
                    +7(902)901-77-94
                </div>
                <div class="header__menu">
                    <span class="header__menu-line"></span>
                    <span class="header__menu-line"></span>
                    <span class="header__menu-line"></span>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style lang="scss">

    @import "../assets/scss/_variable.scss";

    .header {
        height: 100vh;
        background: url("../assets/img/header.jpg") center no-repeat;
        background-size: cover;
    }
    .header-main {
        @extend %center;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        height: calc(100% - 132px);
    }
    .header-block {
        text-align: center;
    }
    .header__title {
        color: #fff;
        text-transform: uppercase;
        line-height: 1;
    }
    .header__subtitle {
        color: #fff;
        text-transform: uppercase;
        line-height: 1;
    }
    .btn {
        outline: none;
        border: none;
        padding: 18px 10px;
        cursor: pointer;
        font-size: 20px;
        text-transform: uppercase;
        border-radius: 5px;
        transition: .5s;
    }
    .btn--orange {
        color: #fff;
        background: $orange;
        &:hover{
            color: $orange;
            background: #fff;
        }
    }
    .header-optionally {
        position: absolute;
        top: 30px;
        right: 0;
        min-width: 250px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .phone {
        color: $gray;
    }
    .header__menu {
        display: flex;
        flex-direction: column;
        cursor: pointer;
    }
    .header__menu-line {
        width: 30px;
        height: 4px;
        background: #fff;
        margin-bottom: 3px;
    }

</style>