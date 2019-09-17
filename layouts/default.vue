<template>
    <nuxt />
</template>

<style lang="less">
  @import "../assets/fonts/style.css";
  @import '../assets/blocks/container/style.less';
  :root {
    --color-font-menu: #000000;
    --color-white: #fff;
    --color-yellow: #f7e611;
    --color-yellow-transparent: rgba(247, 230, 17, .8);
    --font-geometria: 'Geometria';
    --font-geometria-bold: 'Geometria-Bold';
    --font-geometria-medium: 'Geometria-Medium';
    --font-philosopher-regular: 'Philosopher-Regular';
    --font-philosopher-bold: 'Philosopher-Bold';

    --font-size-140: 14rem;
    --font-size-base: 4rem;

    --transition-ease: all .3s;
    --transition-medium: all .7s;
    --transition-slow: all 1.2s;
  }

  *{
      box-sizing: inherit;
  }

  html {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    font-size: 5px;
    @media @min640 {
      font-size: 10px;
    }
    position: relative;
  }
  body{
    margin: 0;
    padding: 0;
  }

</style>
