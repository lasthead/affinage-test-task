<template>

  <div class="container">

    <main-header-base/>
    <main-title class="title-main container__title-main"/>
    <main-slider/>
    <div class="chaplet__wrapper">
      <base-chaplet class="chaplet"/>
    </div>
    <div class="sticker-bottom">
      <span>13</span>
    </div>
  </div>

</template>

<script>
    import MainSlider from "../components/MainSlider";
    import MainHeaderBase from "../components/MainHeaderBase";
    import MainTitle from "../components/MainTitle";
    import BaseChaplet from "../components/BaseChaplet";


    export default {
        name: 'app',
        components: {
            BaseChaplet,
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
      overflow: hidden;
      z-index: 3;
      @media @min768{
        background: transparent;
      }

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

    .chaplet{
      &__wrapper{
        width: 100%;
        display: flex;
        justify-content: center;
      }
      position: absolute;
      bottom: -12.5rem;
      z-index: 10;
      svg{
        width: 25rem;
        height: 25rem;
      }
    }
    .sticker-bottom{
      width: 20rem;
      height: 10rem;
      font-size: var(--font-size-base);
      font-family: var(--font-geometria-bold);
      position: absolute;
      bottom: 0;
      right: 0;
      z-index: 10;
      display: flex;
      align-items: center;
      justify-content: center;
      padding-left: 10rem;
      &::after{
        content: '';
        z-index: -1;
        position: absolute;
        left: 0;
        bottom: 0;
        border-width: 10rem;
        border-style: solid;
        border-color: transparent var(--color-yellow) var(--color-yellow) transparent;
      }
    }
</style>
