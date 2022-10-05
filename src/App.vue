<script setup lang="ts">
  import { useNow, useDateFormat } from "@vueuse/core";

  const formatted = useDateFormat(useNow(), "dddd");
</script>

<template>
  <div
    class="min-w-screen min-h-screen p-4 bg-true-gray-300 text-true-gray-700"
  >
    <header>
      <h1 class="text-3xl font-bold">
        Good
        <h1 class="text-amber-300">{{ formatted }}</h1>
      </h1>
    </header>
  </div>
</template>
