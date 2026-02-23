<script setup lang="ts">
import DailyRoutine from './components/DailyRoutine.vue'
</script>

<template>
  <div class="w-full">
    <div class="w-full flex items-center flex-col justify-center bg-white">
      <h1 class="text-4xl font-bold text-white z-10 absolute text-shadow-lg text-center">
        Hades najlepszy przyjaciel...
      </h1>
      <picture>
        <source srcset="@/assets/hades_head.jpg" media="(min-width: 1024px)" />
        <img src="@/assets/hades_head_mobile.jpg" alt="hades" class="w-full top-0 left-0" />
      </picture>
    </div>

    <DailyRoutine />
  </div>
</template>
