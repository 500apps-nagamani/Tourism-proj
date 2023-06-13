<template>
    <div
      class="fixed inset-x-0 inset-y-0 flex flex-row justify-center bg-[#000000da]"
      @click="$emit('close-modal')"
    >
      <div
        class="flex flex-col items-center mt-auto mb-auto h-3/6 w-1/4 bg-white rounded-md p-10"
        @click.stop
      >
        <img
          src="https://png.pngtree.com/png-vector/20190228/ourmid/pngtree-check-mark-icon-design-template-vector-isolated-png-image_711429.jpg"
          alt=""
          class="w-36"
        />
        <h1 class="text-3xl font-medium mt-3 italic font-sans">
          Congratulations
        </h1>
        <p class="text-xl mt-3">Tour completed Successfully.</p>
        <button
          class="btn bg-[#0ea5e9] w-36 h-10 text-white text-lg py-0 mt-10 rounded-2xl"
          @click="onClickHome"
        >
          Go Home
        </button>
      </div>
      <div class="mt-60 mb-4 ml-4" @click="$emit('close-modal')">
        <img
          src="https://logowik.com/content/uploads/images/close1437.jpg"
          alt=""
          class="w-6"
        />
      </div>
    </div>
</template>


<script setup>
const onClickHome = ()=> navigateTo('/')
</script>