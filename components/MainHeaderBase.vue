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

  .header {
    position: relative;
    padding: 1.5rem 0;
    margin: 0 1rem;
    @media @min768 {
      padding-top: 1.2rem;
    }
    display: flex;
    justify-content: space-between;

    &__menu {
      position: absolute;
      right: 0;
      top: 6rem;
    }
  }
</style>
