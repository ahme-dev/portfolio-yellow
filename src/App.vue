<script setup lang="ts">
  import { useNow, useDateFormat } from "@vueuse/core";

  const formatted = useDateFormat(useNow(), "dddd");
</script>

<template></template>
