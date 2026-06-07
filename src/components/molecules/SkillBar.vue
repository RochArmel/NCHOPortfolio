<template>
  <div class="mt-8">
    <div class="flex items-end justify-between" data-aos="fade-right">
      <h4 class="font-semibold uppercase text-white">{{ label }}</h4>
      <h3 class="text-2xl font-bold text-white">{{ value }}</h3>
    </div>
    <div class="mt-2 h-1 w-full bg-[#131d30] rounded-full">
      <div class="h-1 rounded-full bg-primary" :style="`width: ${value}`"></div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  label: { type: String, required: true },
  value: { type: String, required: true }
});
</script>
