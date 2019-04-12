<template>
  <div>
    <home-header></home-header>
    <home-slider></home-slider>
    <home-icons></home-icons>
  </div>

</template>

<script>
import HomeHeader from './components/Header'
import HomeSlider from './components/Slider'
import HomeIcons from './components/Icons'
    export default {
        name: "home",
        components:{
          HomeHeader:HomeHeader,
          HomeSlider:HomeSlider,
          HomeIcons:HomeIcons
        }
    }
</script>

<style>

</style>
