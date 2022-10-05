<script setup lang="ts">
  import { useNow, useDateFormat } from "@vueuse/core";

  const formatted = useDateFormat(useNow(), "dddd");
</script>

<template>
  <div
    class="min-w-screen min-h-screen bg-true-gray-800 text-true-gray-200 cursor-default select-none"
  >
    <!-- header -->
    <header class="grid md:(grid-cols-2) p-8 h-screen">
      <!-- name -->
      <div class="p-8 flex flex-col gap-8 items-start justify-center">
        <h1 class="text-5xl font-bold">I am Ahmed</h1>
        <p class="text-3xl">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem nam
          repudiandae nemo.
        </p>
      </div>
      <!-- name end -->
      <!-- date -->
      <div class="flex flex-col md:(justify-start) items-end justify-center">
        <h1 class="text-6xl font-bold">Good</h1>
        <h1 class="text-4xl font-bold text-amber-200">
          {{ formatted }}
        </h1>
      </div>
      <!-- date end -->
    </header>
    <!-- header end -->
    <!-- main -->
    <main class="h-screen p-8">
      <h1>Hello</h1>
      <h2>This is new</h2>
    </main>
    <!-- main end -->
  </div>
</template>
