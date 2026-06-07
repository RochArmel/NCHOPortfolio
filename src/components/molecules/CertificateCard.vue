<template>
  <div class="px-8 py-8 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]">
    <div v-if="image" class="mb-5 overflow-hidden rounded-lg border border-[#1f1641] group">
      <img :src="image" :alt="imageAlt" class="w-full h-40 object-cover transition-transform duration-300 group-hover:scale-105">
    </div>
    <div class="flex items-center justify-between">
      <div class="flex items-center gap-2 text-sm text-gray-300">
        <img :src="badgeIcon" alt="badge" class="w-5 h-5">
        <span>{{ issuer }}</span>
      </div>
      <div class="h-10 w-10 rounded-lg bg-primary flex items-center justify-center">
        <img :src="icon" alt="certificate" class="w-5 h-5">
      </div>
    </div>
    <h3 class="pt-6 text-lg font-semibold text-white">{{ title }}</h3>
    <p class="text-gray-300 pt-3 text-sm">{{ description }}</p>
    <button
      v-if="linkLabel"
      type="button"
      class="inline-flex items-center gap-2 pt-4 text-primary hover:text-white"
      @click="emit('view')"
    >
      {{ linkLabel }}
    </button>
  </div>
</template>

<script setup>
const emit = defineEmits(['view']);

defineProps({
  issuer: { type: String, required: true },
  title: { type: String, required: true },
  description: { type: String, required: true },
  icon: { type: String, default: 'https://img.icons8.com/ios-filled/100/ffffff/certificate.png' },
  badgeIcon: { type: String, default: 'https://img.icons8.com/ios-filled/50/22c55e/ok--v1.png' },
  image: { type: String, default: '' },
  imageAlt: { type: String, default: 'certificate' },
  linkLabel: { type: String, default: 'Voir le certificat' }
});
</script>
