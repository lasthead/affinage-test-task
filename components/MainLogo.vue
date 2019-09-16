<template>
<div>
    <span class="logo">A</span>
</div>
</template>

<script>
    export default {
        name: "MainLogo"
    }
</script>

<style scoped lang="less">
    @import '../assets/mixins';

    .logo{
        font-family: var(--font-philosopher-regular);
        color: black;
        font-size: 7.2rem;
        @media @min768{
            font-size: 3.4rem;
        }
    }
</style>
