<script setup lang="ts">
  import { useNow, useDateFormat } from "@vueuse/core";
  import Version from "./components/Version.vue";

  const formatted = useDateFormat(useNow(), "dddd");
</script>

<template>
  <div
    class="min-w-screen min-h-screen bg-true-gray-800 text-true-gray-200 cursor-default select-none"
  >
    <!-- header -->
    <header id="header" class="grid md:(grid-cols-2 p-16) p-8 h-screen">
      <!-- navigate -->
      <nav
        class="flex gap-8 justify-center md:(self-start justify-start)"
        v-motion-fade-visible
        :delay="100"
      >
        <a
          href="#projects"
          class="text-xl font-bold cursor-pointer hover:(text-amber-200)"
          >Projects</a
        >
        <a
          href="#skills"
          class="text-xl font-bold cursor-pointer hover:(text-amber-200)"
          >Skills</a
        >
        <a
          href="#experience"
          class="text-xl font-bold cursor-pointer hover:(text-amber-200)"
          >Experience</a
        >
      </nav>
      <!-- navigate end -->

      <!-- name -->
      <div
        class="flex flex-col gap-8 items-start justify-center md:(self-start)"
        v-motion-fade-visible
        :delay="100"
      >
        <h1 class="text-6xl font-bold">
          I am
          <span class="text-amber-200">Ahmed</span>
        </h1>
        <p class="text-3xl">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem nam
          repudiandae nemo.
        </p>
      </div>
      <!-- name end -->

      <!-- date -->
      <div
        class="flex flex-col md:(justify-start) items-end justify-center md:(row-start-1 col-start-2 row-span-3)"
        v-motion-pop-visible
        :delay="200"
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
        <h1 class="text-6xl font-bold" v-motion-fade-visible :delay="100">
          Projects
        </h1>
        <div class="grid grid-cols-1 md:(grid-cols-2) gap-8">
          <!-- items -->
          <div
            class="flex flex-col gap-4 py-4 border-t-true-gray-700 border-t-8"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            <h2 class="text-3xl italic font-semibold">JournalV</h2>
            <p class="text-2xl">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel non
              rerum nisi, minus est eos voluptas aperiam asperiores?
            </p>
          </div>

          <div
            class="flex flex-col gap-4 py-4 border-t-true-gray-700 border-t-8"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            <h2 class="text-3xl italic font-semibold">Centerm</h2>
            <p class="text-2xl">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel non
              rerum nisi, minus est eos voluptas aperiam asperiores?
            </p>
          </div>

          <div
            class="flex flex-col gap-4 py-4 border-t-true-gray-700 border-t-8"
            v-motion-slide-visible-bottom
            :delay="200"
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
        <h1
          class="text-6xl font-bold text-amber-200"
          v-motion-fade-visible
          :delay="100"
        >
          Skills
        </h1>
        <div class="grid grid-cols-1 md:(grid-cols-3) gap-8">
          <!-- items -->
          <h2
            class="text-3xl italic font-semibold p-4 rounded-2xl bg-amber-200"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            Javascript/Typescript
          </h2>
          <h2
            class="text-3xl italic font-semibold p-4 rounded-2xl bg-amber-200"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            Go
          </h2>
          <h2
            class="text-3xl italic font-semibold p-4 rounded-2xl bg-amber-200"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            Linux
          </h2>
        </div>
      </section>
      <!-- skills end -->
    </main>
    <!-- main end -->
    <Version />
  </div>
</template>
