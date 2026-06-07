<template>
    <section class="text-white mt-18" id="about">
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <SectionHeading title="Plus" highlight="A propos" suffix="de moi" />
                <p class="text-base lg:text-lg mt-8 py-8">
                    Je suis un developpeur web junior front-end passionné par les interfaces claires et les experiences
                    utilisateur simples. J'aime transformer des maquettes en interfaces rapides, accessibles et
                    bien structurées.
                </p>
                <div class="grid grid-cols-3 gap-4 max-w-lg pt-8">
                    <StatCard v-for="stat in stats" :key="stat.label" :value="stat.value" :label="stat.label" />
                </div>
            </div>
            <div class="flex justify-center items-center" data-aos="flip-left">
                <div class="w-64 h-64 sm:w-72 sm:h-72 rounded-full border border-primary p-2">
                    <img src="@/assets/AboutPicture.png" alt="Portrait" class="w-full h-full rounded-full object-cover">
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import SectionHeading from '@/components/molecules/SectionHeading.vue';
import StatCard from '@/components/molecules/StatCard.vue';

const stats = ref([
    //{ value: '+20', label: 'Clients satisfaits' },
    { value: '+2', label: 'Projets' },
    { value: '+1', label: 'Ans d experience' }
]);
</script>
