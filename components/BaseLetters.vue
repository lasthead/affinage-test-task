<template>
  <div class="letter">{{letter}}</div>
</template>

<script>
  export default {
    name: "BaseLetters",
    props: {
      letter: String
    }
  }
</script>

<style lang="less">
  .letter {
    color: transparent;
    -webkit-text-stroke: .2rem var(--color-black);

  }

</style>
