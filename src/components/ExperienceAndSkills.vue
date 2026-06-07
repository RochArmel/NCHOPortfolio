<template>
    <section class="text-white mt-18 relative" id="skills">
        <div class="absolute right-0 top-0 h-full w-full justify-end">
            <span class="flex opacity-20">
                <span class="w-16 h-32 rounded-l-full flex bg-primary blur-2xl"></span>
                <span class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"></span>
            </span>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
                <SectionHeading title="Competences" highlight="techniques" />
                <SkillBar v-for="skill in skills" :key="skill.id" :label="skill.name" :value="skill.width" />
            </div>
            <div data-aos="flip-left">
                <SectionHeading title="Experiences" highlight="professionnelles" align="center" />
                <div class="space-y-8 py-8" data-aos="fade-left">
                    <InfoCard
                        v-for="element in experiences"
                        :key="element.id"
                        :icon="element.icon"
                        :icon-alt="element.iconAlt"
                        :title="element.role"
                        :subtitle="element.company"
                        :meta="element.date"
                    />
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
import SectionHeading from '@/components/molecules/SectionHeading.vue';
import SkillBar from '@/components/molecules/SkillBar.vue';
import InfoCard from '@/components/molecules/InfoCard.vue';

const skills = ref([
    {
        id: 1,
        name: 'HTML & CSS',
        width: '85%'
    },
    {
        id: 2,
        name: 'Vue.js',
        width: '45%'
    },
    {
        id: 3,
        name: 'JavaScript',
        width: '65%'
    },
    {
        id: 4,
        name: 'Figma',
        width: '35%'
    },
    {
        id: 5,
        name: 'Git',
        width: '50%'
    }
]);

const experiences = ref([
    {
        id: 1,
        role: 'Plateforme e-commerce',
        company: 'Boutique en ligne avec panier, paiement et gestion des produits.',
        date: 'Tech: vue.js 3, pinia, express',
        icon: 'https://img.icons8.com/ios-filled/100/ffffff/lawyer.png',
        iconAlt: 'experience icon'
    },
    {
        id: 2,
        role: 'Application mobile',
        company: 'Application mobile pour le suivi des taches quotidiennes.',
        date: 'Tech: vue.js 3, capacitor',
        icon: 'https://img.icons8.com/ios-filled/100/ffffff/lawyer.png',
        iconAlt: 'experience icon'
    },
    {
        id: 3,
        role: 'Dashboard analytics',
        company: 'Tableau de bord pour la visualisation des donnees.',
        date: 'Tech: vue.js 3, chart.js',
        icon: 'https://img.icons8.com/ios-filled/100/ffffff/lawyer.png',
        iconAlt: 'experience icon'
    }
]);
</script>
