<template>
    <div class="header">
        <main-logo/>
        <main-menu-base class="menu header__menu"/>
    </div>
</template>

<script>
    import MainLogo from "../components/MainLogo";
    import MainMenuBase from "../components/MainMenuBase";

    export default {
        name: "MainHeaderBase",
        components: {
            MainMenuBase,
            MainLogo
        }
    }
</script>

<style lang="less" scoped>
    .header{

        display: flex;
        justify-content: space-between;
        &__header-menu{

         }
    }
</style>
