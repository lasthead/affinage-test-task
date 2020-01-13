<template>
  <div>
    <h3 v-if="text">{{text}}</h3>
  </div>
</template>

<script>
  export default {
    name: "BaseSlogan",
    props: {
      text: String
    }
  }
</script>

<style lang="less" scoped>
  h3 {
    font-size: 1.8rem;
    font-family: var(--font-philosopher-regular);
    font-style: italic;
  }
</style>
