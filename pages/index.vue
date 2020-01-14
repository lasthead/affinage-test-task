<template>

  <div class="container">

    <main-header-base/>
    <div class="container__content-centered">
      <main-title class="title-main container__title-main"/>
      <main-slider class="slider__wrapper"/>
    </div>
    <base-slogan :text="slogan" class="slogan"/>
    <div class="chaplet__wrapper">
      <base-chaplet class="chaplet"/>
    </div>
    <div class="container__bottom-symbols bottom-symbols">
      <triangle-philosopher class="symbol symbol__triangle symbol__triangle--bottom"/>
      <triangle-philosopher fill="black" class="symbol symbol__triangle symbol__triangle--top"/>
    </div>
    <yellow-sticker-bookmark class="number-sticker--mobile desktop-hidden"/>
  </div>

</template>

<script>
  import MainSlider from "../components/MainSlider";
  import MainHeaderBase from "../components/MainHeaderBase";
  import MainTitle from "../components/MainTitle";
  import BaseChaplet from "../components/BaseChaplet";
  import BaseLetters from "../components/BaseLetters";
  import TrianglePhilosopher from "../components/TrianglePhilosopher";
  import BaseSlogan from "../components/BaseSlogan";
  import YellowStickerBookmark from "../components/YellowStickerBookmark";
  import BlockEntropyLetters from "../components/BlockEntropyLetters";


  export default {
    name: 'app',
    components: {
      BlockEntropyLetters,
      YellowStickerBookmark,
      BaseSlogan,
      TrianglePhilosopher,
      BaseLetters,
      BaseChaplet,
      MainTitle,
      MainHeaderBase,
      MainSlider
    },
    data() {
      return {
        slogan: 'очень хороший слоган'
      }
    },
    head() {
      return {
        bodyAttrs: {
          class: 'computed-overflow'
        }
      }
    }
  }
</script>

<style lang="less">
  @import '../assets/mixins';

  .computed-overflow {
    overflow: hidden;

    @media @min768 {
      overflow: auto;
    }
  }

  .container {
    background: var(--color-yellow);
    height: 100vh;
    position: relative;
    z-index: 3;
    overflow: hidden;

    @media @min768 {
      background: transparent;
    }

    &__title-main {
      display: none;
      @media @min768 {
        display: block;
      }
      position: absolute;
      width: 100%;
      z-index: 12;
      margin: 23rem 0 0 0;
    }

    &__content-centered {
      display: flex;
      justify-content: center;
    }
  }

  .slider__wrapper {
    width: 100%;
    margin-top: 5rem;
    @media @min768 {
      margin-top: 0;
    }
  }

  .chaplet {
    &__wrapper {
      width: 100%;
      display: flex;
      justify-content: center;
    }

    position: absolute;
    bottom: -12.5rem;
    z-index: 10;

    @media @min768 {
      border-bottom: 1rem solid var(--color-yellow);
      width: 21rem;
      height: 12rem;
      overflow: hidden;
      bottom: 4.5rem;
      position: relative;
    }

    svg {
      width: 24rem;
      height: 24rem;

      @media @min768 {
        width: 21rem;
        height: 17rem;
      }
    }
  }

  .symbol {
    position: absolute;
    z-index: 9;

    &__triangle {
      bottom: 5.7rem;
      left: 9rem;

      &:last-child {
        bottom: auto;
        top: 45rem;
        right: 5.5rem;
        left: auto;
      }
    }
  }

  .slogan {
    position: absolute;
    top: 46rem;
    left: -4rem;
    z-index: 9;
    transform: rotate(270deg);
  }

  .number-sticker {
    &--mobile {
      position: absolute;
    }
  }
</style>
