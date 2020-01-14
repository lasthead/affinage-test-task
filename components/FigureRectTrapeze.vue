<template>
  <div>
    <svg xmlns="http://www.w3.org/2000/svg" width="283" height="178" viewBox="0 0 283 178">
      <defs>
        <clipPath id="b0r8a">
          <path fill="#fff" d="M282.5.5v177l-282-38V.5z"/>
        </clipPath>
      </defs>
      <g>
        <g>
          <path fill="none" stroke="#000" stroke-miterlimit="50" stroke-width="2" d="M282.5.5v177l-282-38v0V.5v0z"
                clip-path="url(&quot;#b0r8a&quot;)"/>
        </g>
      </g>
    </svg>
  </div>
</template>

<script>
  export default {
    name: "FigureRectTrapeze"
  }
</script>

<style lang="less">
  @import '../assets/mixins';

  .figure {
    &__rect {
      width: 56.6rem;
      height: 35rem;

      z-index: 5;

      &--trapeze {
        position: absolute;
        display: inline-block;
        margin-left: -2rem;
        margin-top: 11rem;
        top: -36rem;
        left: 35rem;
        z-index: -1;

        @media @min768 {
          top: -10rem;
          left: 26rem;
          z-index: 9;
          transform: rotate(270deg);
        }
      }
    }
  }
</style>
