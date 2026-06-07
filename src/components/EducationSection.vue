<template>
  <section class="text-white mt-18 relative" id="education">
    <div class="absolute z-0 top-0 inset-x-0 h-64 flex items-start">
      <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"></div>
    </div>
    <div class="py-8 px-4 xl:px-16 relative z-10">
      <div class="md:grid md:grid-cols-2 gap-8 items-start">
        <div>
          <SectionHeading title="Education" />
          <div class="mt-6 flex justify-start">
            <div class="w-72 h-80 sm:w-80 sm:h-96 rounded-3xl border border-primary p-2 bg-primary/10">
              <img src="@/assets/educationPicture.png" alt="Education" class="w-full h-full object-cover rounded-2xl">
            </div>
          </div>
        </div>
        <div>
          <div class="space-y-8 py-8 max-w-2xl" data-aos="flip-right">
            <InfoCard
              v-for="element in education"
              :key="element.id"
              :icon="element.icon"
              :icon-alt="element.iconAlt"
              :title="element.school"
              :subtitle="element.program"
              :meta="element.year"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import SectionHeading from '@/components/molecules/SectionHeading.vue';
import InfoCard from '@/components/molecules/InfoCard.vue';

const education = ref([
  {
    id: 1,
    school: 'ESATIC',
    program: 'Licence DASI',
    year: 'Actuellement',
    icon: 'https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png',
    iconAlt: 'graduation cap'
  },
  {
    id: 2,
    school: 'GROUPE ETIC',
    program: 'BTS IDA',
    year: '2020 - 2021',
    icon: 'https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png',
    iconAlt: 'graduation cap'
  },
    {
    id: 3,
    school: 'GROUPE ETIC',
    program: 'DTS IDA',
    year: '2018 - 2019',
    icon: 'https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png',
    iconAlt: 'graduation cap'
  },
    {
    id: 4,
    school: 'Lycée Simone Gbagbo',
    program: 'Baccalauréat série D',
    year: '2017 - 2018',
    icon: 'https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png',
    iconAlt: 'graduation cap'
  }
]);
</script>
