<template>
  <div class="container">
    <main-header-base/>
    <main-slider/>
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

<style>

</style>
