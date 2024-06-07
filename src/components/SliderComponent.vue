<script>
export default {
  name: 'SliderComponent',
}
</script>

<template>
  <div id="slider-container" class="w-4/5 h-2.5 bg-light-grayish-blue-slider rounded-full absolute mt-14">
    <div id="slider-track" class="absolute top-0 left-0 w-full h-full bg-transparent"></div>
    <div id="slider-thumb" class="absolute top-1/2 -translate-y-1/2 left-1/2 -translate-x-1/2 w-[34px] h-[34px] bg-strong-cyan hover:bg-soft-cyan active:bg-strong-cyan active:cursor-[grabbing] rounded-full cursor-pointer flex justify-center items-center">
      <img class="w-5" src="/src/assets/images/icon-slider.svg" alt="Slider icon">
    </div>
  </div>
</template>