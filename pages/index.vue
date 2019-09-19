<template>

  <div class="container">

    <main-header-base/>
    <main-title class="title-main container__title-main"/>
    <main-slider class="slider__wrapper"/>
    <base-slogan :text="slogan" class="slogan"/>
    <div class="chaplet__wrapper">
      <base-chaplet class="chaplet"/>
    </div>
    <div class="sticker-bottom">
      <span>13</span>
    </div>
    <figure-rect-trapeze class="figure figure__rect figure__rect--trapeze"/>
    <div class="letters">
      <base-letters letter="A" class="letter"/>
      <base-letters letter="G" class="letter"/>
      <base-letters letter="E" class="letter"/>
    </div>
    <triangle-philosopher class="symbol symbol__triangle symbol__triangle--bottom"/>
    <triangle-philosopher fill="black" class="symbol symbol__triangle symbol__triangle--top"/>

  </div>

</template>

<script>
    import MainSlider from "../components/MainSlider";
    import MainHeaderBase from "../components/MainHeaderBase";
    import MainTitle from "../components/MainTitle";
    import BaseChaplet from "../components/BaseChaplet";
    import FigureRectTrapeze from "../components/FigureRectTrapeze";
    import BaseLetters from "../components/BaseLetters";
    import TrianglePhilosopher from "../components/TrianglePhilosopher";
    import BaseSlogan from "../components/BaseSlogan";


    export default {
        name: 'app',
        components: {
            BaseSlogan,
            TrianglePhilosopher,
            BaseLetters,
            FigureRectTrapeze,
            BaseChaplet,
            MainTitle,
            MainHeaderBase,
            MainSlider
        },
        data(){
            return{
                slogan: 'очень хороший слоган'
            }
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
    .slider__wrapper{
      margin-top: 5rem;
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
        width: 24rem;
        height: 24rem;
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

  .figure{
    &__rect{
      width: 56.6rem;
      height: 35rem;

      z-index: 5;
      &--trapeze{
        position: absolute;
        display: inline-block;
        margin-left: -2rem;
        margin-top: 11rem;

        top: -20rem;
        left: 35rem;
        z-index: -1;
      }
    }
  }
  .letters{
    width: 100%;
    display: flex;
    text-align: center;
    justify-content: center;
  }
  .letter{
    position: absolute;
    z-index: 5;

    font-family: var(--font-geometria-medium);
    font-size: 12rem;
    &:first-child{
      top: 45rem;
      left: 13.5rem;
      z-index: 6;
    }
    &:nth-child(2){
      top: 42rem;
      left: 29rem;
    }
    &:nth-child(3){
      top: 26.5rem;
      left: 43.5rem;
      z-index: 6;
    }
  }
  .symbol{
    position: absolute;
    z-index: 9;

    &__triangle{
      bottom: 5.7rem;
      left: 9rem;
      &:last-child{
        bottom: auto;
        top: 45rem;
        right: 5.5rem;
        left: auto;
      }
    }
  }
  .slogan{
    position: absolute;
    top: 46rem;
    left: -4rem;
    z-index: 9;
    transform: rotate(270deg);
  }
</style>
