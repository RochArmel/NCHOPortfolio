<template>
    <section class="text-white mt-20 relative" id="contact">
        <div class="px-4 xl:pl-16">
            <SectionHeading title="Contactez" highlight="moi" />
        </div>
        <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
            <div>
                <p class="text-[#adb7be]">
                    Discutons de votre projet et de la meilleure maniere de le realiser. Je suis disponible pour des
                    missions front-end, des refontes UI et des projets Vue.js.
                </p>
                <div class="col-lg-4 col-md-4 mb-lg-0 mt-5">
                    <ContactItem
                        icon="https://img.icons8.com/metro/50/ffffff/new-post.png"
                        icon-alt="email"
                        label="Email"
                        value="ncho.adomon.roch@gmail.com"
                        link="mailto:ncho.adomon.roch@gmail.com"
                    />
                    <ContactItem
                        icon="https://img.icons8.com/ios-filled/50/ffffff/phone.png"
                        icon-alt="telephone"
                        label="Telephone"
                        value="+225 05 02 12 15 59"
                        link="tel:+2250502121559"
                    />
                    <ContactItem
                        icon="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png"
                        icon-alt="linkedin"
                        label="LinkedIn"
                        value="www.linkedin.com/in/adomon-roch-n-cho-33149023b"
                        link="https://www.linkedin.com/in/adomon-roch-n-cho-33149023b"
                    />
                </div>
            </div>
            <div
            style="background: #111a3e; width: 100%;height: 100%; border-radius: 20px;
            overflow: hidden;border: 1px solid #111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
            <form
                class="flex flex-col p-2"
                data-aos="zoom-in-up"
                action="mailto:ncho.adomon.roch@gmail.com"
                method="GET"
            >
                <div class="mb-6">
                    <label for="email" class="text-white block mb-2 text-sm font-medium">Email</label>
                    <input type="email" id="email" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="email@exemple.com" name="email" required>
                </div>
                <div class="mb-6">
                    <label for="subject" class="text-white block mb-2 text-sm font-medium">Sujet</label>
                    <input type="text" id="subject" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="Sujet" name="subject" required>
                </div>
                <div class="mb-6">
                    <label for="message" class="text-white block mb-2 text-sm font-medium">Message</label>
                    <textarea id="message" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="Parlons de votre projet..." name="message" required></textarea>
                </div>
                <button type="submit" class="z-1 w-[100%!important] px-6 md:px-7 py-3 rounded-full sm:w-max flex justify-center text-white bg-primary border-2 border-transparent transition-all duration-200 hover:scale-[1.02] hover:shadow-lg active:scale-[0.98]">
                    Envoyer le message
                </button>
            </form>
        </div>
        <div class="bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 transform -translate-x-2/3 
        -translate-1/2
        "></div>
        </div>
    </section>
</template>
<script setup>
import SectionHeading from '@/components/molecules/SectionHeading.vue';
import ContactItem from '@/components/molecules/ContactItem.vue';
</script>
