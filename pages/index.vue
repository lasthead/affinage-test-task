<template>

  <div class="container">

    <main-header-base/>
    <main-title class="title-main container__title-main"/>
    <main-slider/>
  </div>

</template>

<script>
    import MainSlider from "../components/MainSlider";
    import MainHeaderBase from "../components/MainHeaderBase";
    import MainTitle from "../components/MainTitle";


    export default {
        name: 'app',
        components: {
            MainTitle,
            MainHeaderBase,
            MainSlider
        }
    }
</script>

<style lang="less">
  @import '../assets/mixins';


    .container{
      background: var(--color-yellow);
      height: 100vh;
      position: relative;
      z-index: 3;

      &__title-main{
        display: none;
        @media @min768{
          display: block;
        }
        position: absolute;
        width: 100%;
        z-index: 5;
      }
    }
    &::before{

      @media @min768{
        content: '';
        display: flex;
        position: absolute;
        height: 50vh;
        left: 10%;
        top: 50%;
        bottom: 0;
        right: 50%;
        z-index: 1;
        box-shadow: 0 0 99px rgba(0, 0, 0, 0.1);
      }
      @media @min1700{
        left: 18%;
      }
    }
    &::after{
      @media @min768{
        content: '';
        display: flex;
        position: absolute;
        height: 100vh;
        left: 50%;
        top: 0;
        bottom: 0;
        right: 0;
        z-index: 2;
        box-shadow: 0 0 99px rgba(0, 0, 0, 0.1);
        background-color: var(--color-white);
      }

    }

</style>
