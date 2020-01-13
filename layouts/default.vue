<template>
  <main>
    <nuxt/>
  </main>
</template>

<style lang="less">
  @import "../assets/fonts/style.css";
  @import '../assets/blocks/container/style.less';

  :root {
    --color-font-menu: #000000;
    --color-white: #fff;
    --color-yellow: #f7e611;
    --color-black: #000000;
    --color-yellow-transparent-light: rgba(247, 230, 17, .8);
    --color-yellow-transparent-dark: rgba(247, 230, 17, .6);
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

  * {
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

  body {
    margin: 0;
    padding: 0;
  }

  main {
    display: flex;
    justify-content: center;

    &::before {

      @media @min768 {
        content: '';
        display: flex;
        position: absolute;
        height: 50vh;
        left: 10%;
        top: 50%;
        bottom: 0;
        right: 50%;
        z-index: 0;
        box-shadow: 0 0 99px rgba(0, 0, 0, 0.1);
      }
      @media @min1700 {
        left: 18%;
      }
    }

    &::after {
      @media @min768 {
        content: '';
        display: flex;
        position: absolute;
        height: 100vh;
        left: 50%;
        top: 0;
        bottom: 0;
        right: 0;
        z-index: 0;
        box-shadow: 0 0 99px rgba(0, 0, 0, 0.1);
        background-color: var(--color-white);
      }

    }
  }
</style>
