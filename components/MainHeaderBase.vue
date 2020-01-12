<template>
    <div>
        <div class="header">
            <main-logo/>
            <main-menu-base class="menu header__menu"/>
        </div>
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
    @import '../assets/mixins';

    .header{

        padding: 1.5rem 4.5rem;
        @media @min768{
            padding-top: 3rem;
        }
        display: flex;
        justify-content: space-between;
        &__header-menu{

         }

    }
</style>
