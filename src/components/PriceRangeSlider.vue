<script setup>

defineProps({
  msg: String,
})

</script>

<template>
  <div class="relative w-screen">
    <div class="w-[90%] max-w-lg absolute mt-[280px] left-1/2 -translate-x-1/2 p-8 flex flex-col items-center bg-white font-manrope rounded-tl-6 rounded-tr-6 shadow-md sm:items-stretch">
      <div class="title-container flex flex-col sm:flex-row sm:justify-between items-center">
        <h3 class="text-grayish-blue font-extrabold text-sm tracking-wider">100K PAGEVIEWS</h3>
        <p class="mt-20 sm:mt-0 text-grayish-blue flex items-center" id="amount-container"><span class="text-3xl font-extrabold text-dark-desaturated-blue mr-3" id="amount">$16.00</span> / month</p>
        <div id="slider-container" class="sm:left-1/2 sm:-translate-x-1/2 w-4/5 h-2.5 bg-light-grayish-blue-slider rounded-full absolute mt-14 sm:mt-28">
          <div id="slider-track" class="absolute top-0 left-0 w-full h-full bg-transparent"></div>
          <div id="slider-thumb" class="absolute top-1/2 -translate-y-1/2 left-1/2 -translate-x-1/2 w-[34px] h-[34px] bg-strong-cyan hover:bg-soft-cyan active:bg-strong-cyan active:cursor-[grabbing] rounded-full cursor-pointer flex justify-center items-center">
            <img class="w-5" src="/src/assets/images/icon-slider.svg" alt="Slider icon">
          </div>
        </div>
      </div>

      <div class="toggle-container flex items-center justify-between text-xs text-grayish-blue mt-7 font-semibold space-x-2 sm:mt-24 sm:ml-20 sm:justify-evenly">
        <p class="monthly">Monthly Billing</p>
        <label class="relative inline-flex cursor-pointer items-center">
          <input id="switch" type="checkbox" class="peer sr-only" />
          <label for="switch" class="hidden"></label>
          <div class="peer h-6 w-11 rounded-full border bg-slate-200 after:absolute after:left-[2px] after:top-0.5 after:h-5 after:w-5 after:rounded-full after:border after:border-gray-300 after:bg-white after:transition-all after:content-[''] peer-hover:bg-soft-cyan peer-checked:bg-soft-cyan peer-checked:after:translate-x-full peer-checked:after:border-white peer-focus:ring-green-300"></div>
        </label>
        <div class="yearly-discount flex items-center justify-between space-x-2">
          <p class="yearly">Yearly Billing</p>
          <div class="px-2 py-1 rounded-xl bg-light-grayish-red text-light-red" id="discount">-25%</div>
        </div>
      </div>

    </div>
  </div>
  
</template>

<style scoped>

</style>
