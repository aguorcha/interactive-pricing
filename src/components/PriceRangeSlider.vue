<script setup>
import { onMounted, ref, watch, computed } from 'vue';

//Añadir texto al #discount para pantallas grandes

let discountElement = null;

onMounted(() => {
  const checkScreenSize = () => {
    if (window.innerWidth > 640 && discountElement) {
      discountElement.textContent += ' discount';
    } else if (discountElement) {
      discountElement.textContent = '-25%';
    }
  }
  window.addEventListener('resize', checkScreenSize);
  checkScreenSize();
});

// Lógica para el arrastre del 'slider-thumb' y modificación reactiva de los datos que se muestran
const sliderContainer = ref(null);

const positions = [
  { position: 0, pageViews: '10K', price: 8 },
  { position: 2, pageViews: '50K', price: 12 },
  { position: 3, pageViews: '100K', price: 16 },
  { position: 4, pageViews: '500K', price: 24 },
  { position: 5, pageViews: '1M', price: 36 }
];

const sliderPosition = ref(0);
const currentPageViews = ref('10K');
const monthlyPrice = ref(8);

</script>

<template>
  <div class="relative w-screen" ref="sliderContainer">
    <div class="w-[90%] max-w-lg absolute mt-[240px] left-1/2 -translate-x-1/2 p-8 flex flex-col items-center bg-white font-manrope rounded-tl-6 rounded-tr-6 shadow-md sm:items-stretch">
      <div class="title-container flex flex-col sm:flex-row sm:justify-between items-center w-full">
        <h3 class="text-grayish-blue font-extrabold text-sm tracking-wider">{{ currentPageViews }} PAGEVIEWS</h3>
        <p id="duration" class="mt-20 sm:mt-0 text-grayish-blue flex items-center"><span
            class="text-3xl font-extrabold text-dark-desaturated-blue mr-3" id="amount">${{ monthlyPrice.toFixed(2) }}</span> / month</p>
      </div>
        <input 
          type="range" 
          min="1" 
          max="5" 
          value="3" 
          id="slider-track"
          class="-mt-20 sm:mt-12"
          >
      <div class="toggle-container flex items-center justify-between text-xs text-grayish-blue mt-[108px] font-semibold space-x-2 sm:mt-14 sm:ml-20 sm:justify-evenly">
        <p class="monthly">Monthly Billing</p>
        <label class="relative inline-flex cursor-pointer items-center">
          <input id="switch" type="checkbox" class="peer sr-only" />
          <label for="switch" class="hidden"></label>
          <div class="peer h-6 w-11 rounded-full border bg-slate-200 after:absolute after:left-[2px] after:top-0.5 after:h-5 after:w-5 after:rounded-full after:border after:border-gray-300 after:bg-white after:transition-all after:content-[''] peer-hover:bg-soft-cyan peer-checked:bg-soft-cyan peer-checked:after:translate-x-full peer-checked:after:border-white peer-focus:ring-green-300">
          </div>
        </label>
        <div class="yearly-discount flex items-center justify-between space-x-2">
          <p class="yearly">Yearly Billing</p>
          <div :class="{ 'add-text-on-large-screens': true }"
            class="px-2 py-1 rounded-xl bg-light-grayish-red text-light-red" id="discount">-25%</div>
        </div>
      </div>

    </div>
  </div>

</template>

<style scoped></style>
