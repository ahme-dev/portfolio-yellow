<script setup lang="ts">
  import { useNow, useDateFormat } from "@vueuse/core";

  const formatted = useDateFormat(useNow(), "dddd");
</script>

<template>
  <div
    class="min-w-screen min-h-screen bg-true-gray-800 text-true-gray-200 cursor-default select-none"
  >
    <!-- header -->
    <header id="header" class="grid md:(grid-cols-2 p-16) p-8 h-screen">
      <!-- navigate -->
      <nav class="flex gap-8 justify-center md:(self-start justify-start)">
        <a href="#projects" class="text-xl font-bold cursor-pointer"
          >Projects</a
        >
        <a href="#skills" class="text-xl font-bold cursor-pointer">Skills</a>
        <a href="#experience" class="text-xl font-bold cursor-pointer"
          >Experience</a
        >
      </nav>
      <!-- navigate end -->

      <!-- name -->
      <div
        class="flex flex-col gap-8 items-start justify-center md:(self-start)"
      >
        <h1 class="text-6xl font-bold">I am Ahmed</h1>
        <p class="text-3xl">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem nam
          repudiandae nemo.
        </p>
      </div>
      <!-- name end -->

      <!-- date -->
      <div
        class="flex flex-col md:(justify-start) items-end justify-center md:(row-start-1 col-start-2 row-span-3)"
      >
        <h1 class="text-6xl font-bold">Good</h1>
        <h1 class="text-4xl font-bold text-amber-200">
          {{ formatted }}
        </h1>
      </div>
      <!-- date end -->

      <!-- waves img -->
      <img
        class="absolute z-0 bottom-0 left-0 opacity-100 w-screen"
        src="./assets/layered-waves-haikei.svg"
      />
      <!-- waves img end -->
    </header>
    <!-- header end -->

    <!-- main -->
    <main id="main" class="min-h-screen text-true-gray-700">
      <!-- projects -->
      <section
        id="projects"
        class="flex flex-col gap-16 min-h-screen bg-amber-200 p-8 md:(p-16)"
      >
        <h1 class="text-6xl font-bold">Projects</h1>
        <div class="grid grid-cols-1 md:(grid-cols-2) gap-8">
          <!-- items -->
          <div
            class="flex flex-col gap-4 py-4 border-t-true-gray-700 border-t-8"
          >
            <h2 class="text-3xl italic font-semibold">JournalV</h2>
            <p class="text-2xl">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel non
              rerum nisi, minus est eos voluptas aperiam asperiores?
            </p>
          </div>

          <div
            class="flex flex-col gap-4 py-4 border-t-true-gray-700 border-t-8"
          >
            <h2 class="text-3xl italic font-semibold">Centerm</h2>
            <p class="text-2xl">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel non
              rerum nisi, minus est eos voluptas aperiam asperiores?
            </p>
          </div>

          <div
            class="flex flex-col gap-4 py-4 border-t-true-gray-700 border-t-8"
          >
            <h2 class="text-3xl italic font-semibold">Gettube</h2>
            <p class="text-2xl">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel non
              rerum nisi, minus est eos voluptas aperiam asperiores?
            </p>
          </div>

          <!-- items end -->
        </div>
      </section>
      <!-- projects end -->

      <!-- skills -->
      <section
        id="skills"
        class="flex flex-col gap-16 min-h-screen p-8 md:(p-16)"
      >
        <h1 class="text-6xl font-bold text-amber-200">Skills</h1>
        <div class="grid grid-cols-1 md:(grid-cols-2) gap-8">
          <div
            class="flex flex-col gap-4 bg-true-gray-700 text-true-gray-200 p-4 rounded-2xl"
          >
            <h2 class="text-3xl italic font-semibold">JournalV</h2>
            <p class="text-2xl">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel non
              rerum nisi, minus est eos voluptas aperiam asperiores?
            </p>
          </div>
        </div>
      </section>
      <!-- skills end -->
    </main>
    <!-- main end -->
  </div>
</template>
