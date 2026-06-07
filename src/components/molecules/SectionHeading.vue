<template>
  <h2 :class="['font-bold text-white', size, alignClass, extraClass]">
    <span>{{ title }}</span>
    <span v-if="highlight" class="ml-2">
      <GradientText>{{ highlight }}</GradientText>
    </span>
    <span v-if="suffix" class="ml-2">{{ suffix }}</span>
  </h2>
</template>

<script setup>
import { computed } from 'vue';
import GradientText from '@/components/atoms/GradientText.vue';

const props = defineProps({
  title: { type: String, required: true },
  highlight: { type: String, default: '' },
  suffix: { type: String, default: '' },
  align: { type: String, default: 'left' },
  size: { type: String, default: 'text-4xl' },
  extraClass: { type: String, default: '' }
});

const alignClass = computed(() => (props.align === 'center' ? 'text-center' : 'text-left'));
</script>
