<template>
  <div class="flex mb-10 items-center">
    <div class="p-2" style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%; overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
      <img :src="icon" :alt="iconAlt" class="w-6">
    </div>
    <div class="ml-5 text-white">
      <h4>{{ label }}</h4>
      <p v-if="link">
        <a :href="link" class="text-primary hover:text-white" target="_blank" rel="noopener noreferrer">
          {{ value }}
        </a>
      </p>
      <p v-else>{{ value }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  icon: { type: String, required: true },
  iconAlt: { type: String, default: 'icon' },
  label: { type: String, required: true },
  value: { type: String, required: true },
  link: { type: String, default: '' }
});
</script>
