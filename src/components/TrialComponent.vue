<script setup>

defineProps({
  msg: String,
})

</script>

<template>
  <div class="relative w-screen">
    <div class="w-[90%] max-w-lg absolute mt-[534px] sm:mt-[502px] left-1/2 -translate-x-1/2 p-8 flex flex-col items-center sm:flex-row sm:justify-between sm:px-12 bg-white font-manrope rounded-bl-6 rounded-br-6 shadow-md">
      <div class="data flex flex-col items-center text-xs font-semibold text-grayish-blue sm:items-start">
        <div class="flex">
          <img class="w-3 h-3 mt-1" src="/src/assets/images/icon-check.svg" alt="Check Icon">
          <p class="ml-4 mb-2">Unlimited websites</p>
        </div>
        <div class="flex">
          <img class="w-3 h-3 mt-1" src="/src/assets/images/icon-check.svg" alt="Check Icon">
          <p class="ml-4 mb-2">100% data ownership</p>
        </div>
        <div class="flex">
          <img class="w-3 h-3 mt-1" src="/src/assets/images/icon-check.svg" alt="Check Icon">
          <p class="ml-4 mb-2">Email reports</p>
        </div>
      </div>
      <button class="px-12 py-2.5 mt-6 bg-dark-desaturated-blue text-pale-blue text-xs font-bold rounded-3xl sm:mb-6">Start my trial</button>
    </div>
  </div>
</template>

<style scoped>

</style>