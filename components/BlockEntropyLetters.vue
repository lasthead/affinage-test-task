<template>
  <div class="letters">
    <base-letters letter="A" class="letter"/>
    <base-letters letter="G" class="letter"/>
    <base-letters letter="E" class="letter"/>
  </div>
</template>

<script>
  import BaseLetters from "./BaseLetters";

  export default {
    name: "BlockEntropyLetters",
    components: {BaseLetters}
  }
</script>

<style lang="less">
  @import '../assets/mixins';

  .letters {
    width: 100%;
    display: flex;
    text-align: center;
    justify-content: center;
  }

  .letter {
    position: absolute;
    z-index: 5;

    font-family: var(--font-geometria-medium);
    font-size: 11rem;

    @media @min768 {
      font-size: 7rem;
    }

    &:first-child {
      top: 32rem;
      left: 13.5rem;
      z-index: 7;

      @media @min768 {
        top: -5rem;
        left: auto;
        right: 41rem;
      }
    }

    &:nth-child(2) {
      top: 30rem;
      left: 29rem;

      @media @min768 {
        top: 9rem;
        left: auto;
        right: 31rem;
        z-index: 9;
      }
    }

    &:nth-child(3) {
      top: 15.5rem;
      left: 43.5rem;
      z-index: 6;

      @media @min768 {
        top: 2rem;
        left: auto;
        right: 23rem;
        z-index: 5;
      }
    }
  }
</style>
