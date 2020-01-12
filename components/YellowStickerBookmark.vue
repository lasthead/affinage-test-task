<template>
  <div class="bookmark">
    <span>13</span>
  </div>
</template>

<script>
  export default {
    name: "YellowStickerBookmark"
  }
</script>

<style scoped lang="less">
  @import '../assets/mixins';

  .bookmark{
    width: 13.9rem;
    height: 10rem;
    font-size: var(--font-size-base);
    font-family: var(--font-geometria-bold);
    bottom: 0;
    right: 0;
    z-index: 10;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-left: 7rem;
  &::after{
    content: '';
    z-index: -1;
    position: absolute;
    left: 0;
    bottom: 0;
    border-width: 7.3rem;
    border-style: solid;
    border-color: transparent var(--color-yellow) var(--color-yellow) transparent;
   }
  @media @min768 {
    right: auto;
    width: 13.8rem;
    height: 38.3rem;
    background-color: var(--color-yellow);
    padding-left: 0;

  &::after {
     display: none;
   }
  }
  }
</style>
