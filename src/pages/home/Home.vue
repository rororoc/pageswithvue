<template>
  <div>
    <home-header></home-header>
    <home-slider></home-slider>
    <home-icons></home-icons>
    <home-like></home-like>
  </div>

</template>

<script>
import HomeHeader from './components/Header'
import HomeSlider from './components/Slider'
import HomeIcons from './components/Icons'
import HomeLike from './components/Like'
    export default {
        name: "home",
        components:{
          HomeHeader:HomeHeader,
          HomeSlider:HomeSlider,
          HomeIcons:HomeIcons,
          HomeLike:HomeLike
        }
    }
</script>

<style>

</style>
