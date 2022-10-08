<script setup lang="ts">
  import { ref } from "vue";

  const formData = ref({
    fullname: "",
    email: "",
    message: "",
  });
</script>

<template>
  <div class="grid gap-4 md:(px-8) lg:(grid-cols-2)">
    <!-- contact form -->
    <form
      action="post"
      class="flex flex-col items-center gap-4 bg-true-gray-700 text-true-gray-200 p-4 md:(p-8 items-end) rounded-2xl"
    >
      <div
        class="flex flex-col gap-4 justify-start md:(justify-center flex-row items-center)"
      >
        <label class="font-semibold" for="fullname">Fullname:</label>
        <input
          v-model="formData.fullname"
          class="rounded-2xl px-4 py-2 border-2 w-full border-transparent focus:(border-amber-200 border-2)"
          type="text"
          placeholder="John Smith"
          name="fullname"
        />
      </div>
      <div
        class="flex flex-col gap-4 justify-start md:(justify-center flex-row items-center)"
      >
        <label class="font-semibold" for="email">Email:</label>
        <input
          v-model="formData.email"
          required
          class="rounded-2xl px-4 py-2 w-full border-2 border-transparent focus:(border-amber-200 border-2)"
          type="email"
          name="email"
          placeholder="johnsmith@gmail.com"
        />
      </div>
      <div
        class="flex flex-col gap-4 justify-start md:(justify-center flex-row items-center)"
      >
        <label class="font-semibold" for="message">Message:</label>
        <textarea
          v-model="formData.message"
          required
          placeholder="I wanna hire you"
          class="rounded-2xl px-4 py-2 resize-y h-34 border-2 w-full border-transparent focus:(border-amber-200 border-2)"
          name="message"
        />
      </div>
      <input
        class="px-4 py-2 rounded-2xl cursor-pointer hover:(duration-300 bg-amber-200 text-true-gray-700)"
        type="submit"
        value="Submit"
      />
    </form>
    <!-- contact form end -->

    <!-- contact preview -->
    <div
      class="flex flex-col gap-4 bg-true-gray-700 text-true-gray-200 p-4 md:(p-8) rounded-2xl text-lg"
    >
      <h1 class="font-bold">New Message!</h1>

      <p
        class="border-l-amber-200 border-l-3 px-2 italic text-xl overflow-y-scroll max-h-54"
        v-if="formData.message"
      >
        {{ formData.message }}
      </p>

      <div
        v-if="formData.email || formData.fullname"
        class="flex flex-wrap gap-2"
      >
        <h1>
          From
          <span class="text-amber-200 italic font-semibold"
            >{{ formData.fullname }}
          </span>
        </h1>

        <h2
          v-if="formData.email"
          class="bg-amber-200 text-true-gray-700 px-2 rounded-xl"
        >
          {{ formData.email }}
        </h2>
      </div>
    </div>
    <!-- contact preview end -->
  </div>
</template>
