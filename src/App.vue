<script setup lang="ts">
import DailyRoutine from './components/DailyRoutine.vue'
</script>

<template>
  <div class="w-full">
    <div class="w-full flex items-center flex-col justify-center bg-white">
      <h1 class="text-4xl font-bold text-white z-10 absolute text-shadow-lg text-center">
        Hades najlepszy przyjaciel...
      </h1>
      <img src="@/assets/hades_head.jpg" alt="Hades the dog" class="w-full top-0 -let-0" />
    </div>

    <DailyRoutine />
  </div>
</template>
