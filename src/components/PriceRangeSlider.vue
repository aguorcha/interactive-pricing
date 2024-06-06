<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <div class="relative w-screen">
    <div class="container absolute w-9/10 max-w-[500px] mt-[280px] left-1/2 -translate-x-1/2 p-8 flex flex-col items-center bg-white font-manrope rounded-tl-6 rounded-tr-6">
      <div class="title-container flex flex-col items-center">
        <h3 class="text-grayish-blue font-extrabold text-sm tracking-wider">100K PAGEVIEWS</h3>
        <div class="">
          <p class="mt-20 text-grayish-blue flex items-center" id="amount-container"><span class="text-3xl font-extrabold text-dark-desaturated-blue mr-3" id="amount">$16.00</span> / month</p>
        </div>
        
        <div id="slider-container" class="w-4/5 h-2.5 bg-light-grayish-blue-slider rounded-full absolute mt-14">
          <div id="slider-track" class="absolute top-0 left-0 w-full h-full bg-transparent"></div>
          <div id="slider-thumb" class="absolute top-1/2 -translate-y-1/2 left-1/2 -translate-x-1/2 w-[34px] h-[34px] bg-strong-cyan hover:bg-soft-cyan active:bg-strong-cyan active:cursor-[grabbing] rounded-full cursor-pointer flex justify-center items-center">
            <img class="w-5" src="/src/assets/images/icon-slider.svg" alt="Slider icon">
          </div>
        </div>
      </div>
      <div id="track"></div>
    </div>
  </div>
  
</template>

<style scoped>

  .container {
    /* position: absolute; */
    width: 90%;
    /* max-width: 500px;
    margin-top: 280px;
    left: 50%;
    transform: translateX(-50%);
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    font-family: 'Manrope', sans-serif;
    border-radius: 6px 6px 0 0; */
  }
  /* #slider-container {
    width: 80%;
    height: 10px;
    background-color: #eee;
    border-radius: 10px;
    position: absolute;
    margin-top: 54px;
  } */
  /* #slider-track {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: transparent;
  }
  #slider-thumb {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    left: 44%;
    width: 34px;
    height: 34px;
    background-color: green;
    border-radius: 50%;
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  #slider-thumb img {
    width: 20px;
  } */
</style>
