<script setup lang="ts">
  import { useNow, useDateFormat } from "@vueuse/core";
  import { info, skills, projects } from "./info";
  import Contact from "./components/Contact.vue";

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
        <a
          v-for="el in ['Projects', 'Skills', 'Contact']"
          :href="'#' + el.toLocaleLowerCase()"
          class="text-xl p-2 font-bold cursor-pointer hover:(text-amber-200 duration-300 duration-300)"
          >{{ el }}
        </a>
      </nav>
      <!-- navigate end -->

      <!-- name -->
      <div
        class="flex flex-col gap-8 items-start justify-center md:(self-start)"
      >
        <h1 class="text-5xl font-bold">
          I am
          <span class="text-amber-200">{{ info.name }}</span>
        </h1>
        <p class="text-2xl">{{ info.about }}</p>
      </div>
      <!-- name end -->

      <!-- date -->
      <div
        class="flex flex-col md:(justify-start) items-end justify-center md:(row-start-1 col-start-2 row-span-3)"
        v-if="formatted"
      >
        <h1 class="text-5xl font-bold">Good</h1>
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
        <h1 class="text-5xl font-bold" v-motion-fade-visible :delay="100">
          Projects
        </h1>
        <div class="grid grid-cols-1 md:(grid-cols-2 px-8) gap-8">
          <!-- items -->
          <div
            v-for="el in projects"
            class="flex flex-col gap-4 p-4 border-t-true-gray-700 border-t-8 hover:(shadow-xl duration-300 cursor-pointer bg-true-gray-700 text-true-gray-200)"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            <h2 class="text-2xl italic font-semibold">{{ el }}</h2>
            <p class="text-xl">
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
          class="text-5xl font-bold text-amber-200"
          v-motion-fade-visible
          :delay="100"
        >
          Skills
        </h1>
        <div class="grid grid-cols-1 md:(grid-cols-3 px-8) gap-8">
          <!-- items -->
          <h2
            v-for="el in skills"
            class="text-2xl italic font-semibold p-4 rounded-2xl bg-amber-200 hover:(shadow-xl duration-300 cursor-pointer)"
            v-motion-slide-visible-bottom
            :delay="200"
          >
            {{ el }}
          </h2>
        </div>
      </section>
      <!-- skills end -->
    </main>
    <!-- main end -->

    <!-- footer -->
    <footer id="footer" class="text-true-gray-700 min-h-screen">
      <!-- contact -->
      <section
        id="contact"
        class="flex flex-col gap-16 min-h-screen p-8 md:(p-16) bg-amber-200 text-xl"
      >
        <h1 class="text-5xl font-bold" v-motion-fade-visible :delay="100">
          Contact
        </h1>
        <Contact v-motion-slide-visible-bottom></Contact>
      </section>
      <!-- contact end -->
      <section
        id="contact"
        class="flex flex-col items-start justify-evenly gap-4 p-8 md:(p-16 flex-row) text-xl text-true-gray-400"
      >
        <div>
          <h1>Email: ahmadkabdullah@pm.me</h1>
          <h1>Phone: 0770 123 4567</h1>
        </div>
        <div>
          <h1>
            Source:
            <a href="https://github.com/ahmedkapro/portfolio-yellow">
              github.com/ahmedkapro/portfolio-yellow
            </a>
          </h1>
        </div>
      </section>
    </footer>
    <!-- footer end -->
  </div>
</template>
