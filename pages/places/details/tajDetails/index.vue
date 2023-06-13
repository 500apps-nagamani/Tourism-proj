<template>
  <div class="flex flex-row h-screen">
    <div class="flex flex-col w-1/4 bg-[#60a5fa] rounded-md p-4 overflow-y-auto">
      <h1 class="text-3xl italic font-serif mb-4">Relative images</h1>
      <div v-for="pic in imagesList" :key="index">
        <img :src= 'pic' class="w-full border border-white mb-2" />
      </div>
    </div>

    <div class="bg-[#cbd5e1] p-4" >
      <h1 class="text-4xl italic text-[#1e3a8a] m-4">Detailed View</h1>

      <img
        src="https://d1tgh8fmlzexmh.cloudfront.net/ccbp-static-website/tajmahal-c1-img.png"
        class="w-50 h-50 m-4"
      />

      <h1 class="text-xl italic text-[#1e3a8a] m-4">Tajmahal</h1>

      <p class="m-4">
        “The embodiment of all things pure”, said Rudyard Kipling on Taj Mahal’s
        beauty and that is no wordplay as the Taj is undoubtedly a pure epitome
        of beauty.
        <br />It is an immortal poem in white marble and is the finest
        expression of love of an emperor for his queen. Located on a bank of
        River Yamuna, it was built by Mughal Emperor Shah Jahan
      </p>
      <button class="btn m-4" @click="changeView">Tour completed</button>
      <button class="btn bg-[#1d4ed8]" @click="onForm">Show Form</button>
    </div>
    <SaveModal v-show="showModal" @close-modal="showModal = false" />
    <SlideOutModal v-show="showForm" @close-form="showForm = false" />
  </div>
</template>

<script setup>
import SaveModal from "~/components/SaveModal.vue";
// import SlideOutModal from "~/components/SlideOutModal";

definePageMeta({
  layout: "placesdetails",
});

const showModal = ref(false);
const showForm = ref(false);
const changeView = () => (showModal.value = true);
const onForm = () => (showForm.value = true);

const imagesList = [
  "https://cdn.pixabay.com/photo/2015/07/29/22/56/taj-mahal-866692_1280.jpg",
  "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQkEcV3H4DozvihDCegYwnvzjckDw8w9M9u9Q&usqp=CAU",
  "https://media.istockphoto.com/id/1208049833/photo/amazing-view-on-the-taj-mahal-in-sunset-light-with-reflection-in-water-the-taj-mahal-is-an.jpg?s=612x612&w=0&k=20&c=rNo7Q1k7SSaH6T09HShS57X9dw2QkuRBcnP2dNxAGIE=",
  "https://www.jagranimages.com/images/newimg/26092022/26_09_2022-tajmahal_agra_23100550.webp",
  "https://media-cdn.tripadvisor.com/media/photo-s/1a/70/5e/24/caption.jpg",
  "https://s01.sgp1.cdn.digitaloceanspaces.com/article/183907-awptpwkudq-1670237885.jpg",
  "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRCpvW-0C2UPLOLveRahQ7hE9B34_fBuyfS6g&usqp=CAU",
];

</script>

<style scoped></style>
