<template>
  <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
    <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">{{ value }}</h3>
    <p class="text-sm sm:text-base text-gray-300">{{ label }}</p>
  </div>
</template>

<script setup>
defineProps({
  value: { type: String, required: true },
  label: { type: String, required: true }
});
</script>
