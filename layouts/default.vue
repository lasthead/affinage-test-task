<template>
  <div>
    <nuxt />
  </div>
</template>

<style lang="less">
  @import "../assets/fonts/style.css";
  @import '../assets/blocks/container/style.less';
  :root {
    --color-font-menu: #000000;

    --font-geometria: 'Geometria';
    --font-geometria-bold: 'Geometria-Bold';
    --font-geometria-medium: 'Geometria-Medium';
    --font-philosopher-regular: 'Philosopher-Regular';

    --transition-ease: all .3s;
    --transition-medium: all .7s;
    --transition-slow: all 1.2s;
  }

  html {
    font-size: 5px;
    @media @min640 {
      font-size: 10px;
    }
    position: relative;
  }
</style>
