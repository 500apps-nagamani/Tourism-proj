<template>
  <div class="m-0">
    <header>
      <nav class="bg-[#94a3b8] p-3">
        <ul class="flex text-xl text-white items-center">
          <li class="ml-2">
            <NuxtLink to="/"> Home </NuxtLink>
          </li>
          <li class="ml-4">
            <NuxtLink to="/places"> Places </NuxtLink>
          </li>
          <Menu as="div" class="relative inline-block text-left">
         <div>
            <MenuButton  class="inline-flex flex-col w-full justify-center items-center gap-x-1 rounded-md bg-skin-white ml-4 py-3 px-1 text-sm font-semibold shadow-sm border border-skin-secondary/20 hover:bg-skin-base/10">
              
              <!-- <ChevronDownIcon /> -->
              <hr class="w-3 mt-1"/>
              <hr class="w-3 mt-1"/>
              <hr class="w-3 mt-1"/>
            </MenuButton>
          </div> 
            
          <MenuItems class="absolute mt-2 w-40 origin-top-right divide-y divide-skin-base/10 rounded-md bg-skin-white shadow-lg border border-skin-secondary/20 focus:outline-none z-20">
            <div class="px-1 py-1 bg-white">
              <MenuItem v-slot="{ active }" class="border-b">
                <button
                    class='group flex w-full items-center rounded-md px-2 py-2 text-sm font-bold text-[#475569]'
                  
                      @click="onTaj"
                  >

                    <span
                      :active="active"
                      class="fa-duotone fa-list mr-2 h-5 w-5 flex items-center justify-center text-[#475569]"
                      aria-hidden="true"
                    />
                   Tajmahal
                  </button>
              </MenuItem>
              <MenuItem v-slot="{ active }" class="border-b">
                  <button
                    class='group flex w-full items-center rounded-md px-2 py-2 text-sm font-bold text-[#334155]'
                    
                    @click="onMysore"

                  >
                    <span
                      :active="active"
                      class="fa-duotone fa-book-open-cover flex items-center justify-center mr-2 h-5 w-5"
                      aria-hidden="true"
                    />
                   Mysore palace
                  </button>
                </MenuItem>
            </div>
          </MenuItems>
      
           
          </Menu>
        </ul>
      </nav>
    </header>
      <slot />
   
  </div>
</template>

<script setup lang="ts">
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";

// import { ChevronDownIcon } from "@vue-hero-icons/outline"

const onTaj = ()=> navigateTo('/places/details/tajDetails')
const onMysore = ()=> navigateTo('/places/details/mysoreDetails')


</script>

<style scoped>
.router-link-exact-active {
  text-decoration: underline;
  color: brown;
}
</style>
