<template>
  <div
    class="fixed inset-x-0 inset-y-0 bg-[#000000da] flex flex-col justify-center items-center"
    @click="$emit('close-form')"
  >
    <div class="bg-white h-full w-1/4 rounded-md ml-auto" @click.stop>
        <h1 class="m-4 text-3xl font-serif">Form</h1>
      <form class="flex flex-col p-4">
        <label for="fname">First Name</label>
        <input
          type="text"
          id="fname"
          class="border border-gray-500 w-40 mb-4"
        />
        <label for="lname">Last Name</label>
        <input
          type="text"
          id="lname"
          class="border border-gray-500 w-40 mb-4"
        />
        <label for="gen">Gender</label>
        <div id="gen">
          <input type="radio" name="group" id="m" class="m-2" />
          <label for="m">Male</label>
          <input type="radio" name="group" id="f" class="m-2 ml-4" />
          <label for="f">Feale</label>
        </div>
        <button class="btn w-20 bg-[#1d4ed8] mt-4" type="submit" @click="$emit('close-form')">Submit</button>
      </form>
    </div>
  </div>
</template>

