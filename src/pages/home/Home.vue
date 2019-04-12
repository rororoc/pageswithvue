<template>
  <div>
    <home-header></home-header>
    <home-slider></home-slider>
  </div>

</template>

<script>
import HomeHeader from './components/Header'
import HomeSlider from './components/Slider'
    export default {
        name: "home",
        components:{
          HomeHeader:HomeHeader,
          HomeSlider:HomeSlider
        }
    }
</script>

<style>

</style>
