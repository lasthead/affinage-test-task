<template>
  <div class="main">
  <div class="container">
      <main-header-base/>
      <main-slider/>
  </div>
  </div>
</template>

<script>
    import MainSlider from "../components/MainSlider";
    import MainHeaderBase from "../components/MainHeaderBase";


    export default {
        name: 'app',
        components: {
            MainHeaderBase,
            MainSlider
        }
    }
</script>

<style lang="less">
  .main{
    height: 100vh;
    position: relative;
    .container{
      position: relative;
      z-index: 3;
    }
    &::before{
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
    &::after{
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
