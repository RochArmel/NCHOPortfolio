<template>
  <section class="text-white mt-20" id="certifications">
    <div class="px-4 xl:pl-16">
      <SectionHeading title="Certifications" />
    </div>
    <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3">
      <CertificateCard
        v-for="certificate in certificates"
        :key="certificate.id"
        :issuer="certificate.issuer"
        :title="certificate.title"
        :description="certificate.description"
        :image="certificate.image"
        :image-alt="certificate.imageAlt"
        :link-label="certificate.linkLabel"
        @view="openModal(certificate)"
      />
    </div>
    <div
      v-if="selectedCertificate"
      class="fixed inset-0 z-50 flex items-center justify-center bg-black/70 px-4"
      @click="closeModal"
    >
      <div class="w-full max-w-4xl rounded-2xl bg-[#111a3e] border border-[#1f1641] p-4" @click.stop>
        <div class="flex items-center justify-between pb-4">
          <div>
            <h3 class="text-xl font-semibold text-white">{{ selectedCertificate.title }}</h3>
            <p class="text-sm text-gray-300">{{ selectedCertificate.issuer }}</p>
          </div>
          <button type="button" class="text-white text-2xl" @click="closeModal">x</button>
        </div>
        <div class="overflow-hidden rounded-xl border border-[#1f1641]">
          <img
            :src="selectedCertificate.image"
            :alt="selectedCertificate.imageAlt"
            class="w-full max-h-[70vh] object-contain bg-black"
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import SectionHeading from '@/components/molecules/SectionHeading.vue';
import CertificateCard from '@/components/molecules/CertificateCard.vue';

const certificates = ref([
  {
    id: 1,
    issuer: 'Udemy',
    title: 'HTML CSS Bootstrap',
    description: 'Certification HTML CSS Bootstrap.',
    image: 'src/assets/UC-HTMLCSSBootstrap.jpg',
    imageAlt: 'Certificat HTML CSS Bootstrap',
    linkLabel: 'Voir le certificat'
  },
  {
    id: 2,
    issuer: 'Udemy',
    title: 'Flask',
    description: 'Creation de projets complets avec Flask.',
    image: 'src/assets/UC-flask.jpg',
    imageAlt: 'Certificat Flask',
    linkLabel: 'Voir le certificat'
  },
  {
    id: 3,
    issuer: 'Udemy',
    title: 'Git',
    description: 'Certification sur l utilisation de Git.',
    image: 'src/assets/UC-Git.jpg',
    imageAlt: 'Certificat Git',
    linkLabel: 'Voir le certificat'
   }
]);

const selectedCertificate = ref(null);

const openModal = (certificate) => {
  selectedCertificate.value = certificate;
};

const closeModal = () => {
  selectedCertificate.value = null;
};
</script>
