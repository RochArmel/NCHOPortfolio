<template>
  <div class="flex items-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]">
    <div class="w-1/4">
      <img :src="icon" :alt="iconAlt" />
    </div>
    <div class="w-3/4 pl-4">
      <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
        {{ title }}
      </h3>
      <p class="text-white">{{ subtitle }}</p>
      <p v-if="meta" class="text-white">{{ meta }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  icon: { type: String, required: true },
  iconAlt: { type: String, default: 'item icon' },
  title: { type: String, required: true },
  subtitle: { type: String, required: true },
  meta: { type: String, default: '' }
});
</script>
