<template>
  <div class="flex h-screen">
    <div
      class="flex flex-col w-5/12 bg-[#60a5fa] rounded-md p-4 overflow-y-auto"
    >
      <h1 class="text-3xl italic font-serif mb-4">Relative images</h1>
      <div v-for="pic in imagesList" :key="index">
        <img :src="pic" class="w-fit border border-white mb-2" />
      </div>
    </div>

    <div class="bg-[#cbd5e1] p-4">
      <h1 class="text-4xl italic text-[#1e3a8a] m-4">Detailed View</h1>

      <img
        src="https://d1tgh8fmlzexmh.cloudfront.net/ccbp-static-website/mysore-palace1-img.png"
        class="w-50 h-50 m-4"
      />

      <h1 class="text-xl italic text-[#1e3a8a] m-4">Mysore Palace</h1>

      <p class="m-4">
        The embodiment of all things pure”, said Rudyard Kipling on Taj Mahal’s
        beauty and that is no wordplay as the Taj is undoubtedly a pure epitome
        of beauty. It is an immortal poem in white marble and is the finest
        expression of love of an emperor for his queen. Located on a bank of
        River Yamuna, it was built by Mughal Emperor Shah
      </p>
      <button class="btn m-4" @click="changeView">Completed Tour</button>
      <button class="btn bg-[#1d4ed8]" @click="onForm">Show Form</button>
      <SaveModal v-show="showModal" @close-modal="showModal = false" />
      <SlideOutModal v-show="showForm" @close-form="showForm = false" />
    </div>
  </div>
</template>

<script setup>
import SaveModal from "~/components/SaveModal.vue";
import SlideOutModal from "~/components/SlideOutModal";

definePageMeta({
  layout: "placesdetails",
});

const showModal = ref(false);
const showForm = ref(false);
const changeView = () => (showModal.value = true);
const onForm = () => (showForm.value = true);

const imagesList = [
  "https://www.holidify.com/images/cmsuploads/compressed/attr_1568_20191102174918.jpg",
  "https://karnatakatourism.org/wp-content/uploads/2020/06/Mysuru-Palace-banner-1920_1100.jpg",
  "https://images.pexels.com/photos/7417029/pexels-photo-7417029.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
  "https://bangalore247.in/wp-content/uploads/2021/03/Mysore-Palace.jpg",
  "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT1cKMwZw7yY14prG8n7Hyg_mYmyaFNJflTLg&usqp=CAU",
  "https://th-i.thgim.com/public/migration_catalog/article11567134.ece/alternates/FREE_1200/13BGPALACE_ILLUMINATION",
  "https://i0.wp.com/www.tusktravel.com/blog/wp-content/uploads/2021/02/Durbar-Hall-Mysore-Palace.jpeg?fit=800%2C532&ssl=1",
];
</script>

<style scoped></style>
