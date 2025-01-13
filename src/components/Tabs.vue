<script setup>
import { ref } from 'vue'
import Home from './Home.vue';
import Event from './Event.vue';
import Boss from './Boss.vue';
import Products from './Products.vue';
import Gallery from './Gallery.vue';

let tab = ref(0);
let isDropdownOpen = ref(false);

const toggleDropdown = () => {
  isDropdownOpen.value = !isDropdownOpen.value;
};
</script>

<!-- Tabs per la navigazione -->
<template>
  <div class="w-full">
    <div class="flex justify-between p-5">
      <div @click="tab = 0">
        <img class="imglogo" src="../media/logo.jpg" alt="logo" width="100">
      </div>

      <!-- Pulsante a tendina per dispositivi mobili -->
      <div class="relative sm:hidden">
        <button @click="toggleDropdown" class="btn btn-xs text-white">
          Menu
        </button>
        <div v-if="isDropdownOpen" class="absolute right-0 mt-2 w-48 bg-white border rounded-lg shadow-lg z-10">
          <button
            @click="tab = 1"
            :class="{'btn-neutral' : tab === 1}"
            class="block w-full text-left px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">
            HOME
          </button>
          <button
            @click="tab = 2"
            :class="{'btn-neutral' : tab === 2}"
            class="block w-full text-left px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">
            PRODOTTI
          </button>
          <button
            @click="tab = 3"
            :class="{'btn-neutral' : tab === 3}"
            class="block w-full text-left px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">
            PROPRIETARIO
          </button>
          <button
            @click="tab = 4"
            :class="{'btn-neutral' : tab === 4}"
            class="block w-full text-left px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">
            GALLERIA
          </button>
          <button
            @click="tab = 5"
            :class="{'btn-neutral' : tab === 5}"
            class="block w-full text-left px-4 py-2 text-sm text-gray-700 hover:bg-gray-100">
            EVENTI
          </button>
        </div>
      </div>

      <!-- Pulsanti regolari per dispositivi più grandi -->
      <div class="hidden sm:flex space-x-20">
        <button
          @click="tab = 1"
          :class="{'btn-neutral' : tab === 1}"
          class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg">
          HOME
        </button>
        <button
          @click="tab = 2"
          :class="{'btn-neutral' : tab === 2}"
          class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg">
          PRODOTTI
        </button>
        <button
          @click="tab = 3"
          :class="{'btn-neutral' : tab === 3}"
          class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg">
          PROPRIETARIO
        </button>
        <button
          @click="tab = 4"
          :class="{'btn-neutral' : tab === 4}"
          class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg">
          GALLERIA
        </button>
        <button
          @click="tab = 5"
          :class="{'btn-neutral' : tab === 5}"
          class="btn btn-xs sm:btn-sm md:btn-md lg:btn-lg">
          EVENTI
        </button>
      </div>
    </div>

    <!-- Contenuto -->
    <div>
      <div v-if="tab === 0" class="py-10 px-6">

        <Home />

      </div>

      <div v-if="tab === 1" class="py-10 px-6">

        <Home />

      </div>
      <div v-if="tab === 2" class="py-10 px-6">

        <Products />

      </div>
      <div v-if="tab === 3" class="py-10 px-6">

        <Boss/>

      </div>
      <div v-if="tab === 4" class="py-10 px-6">

        <Gallery />
      </div>
      <div v-if="tab === 5" class="py-10 px-6">

        <Event/>

      </div>
    </div>
  </div>
</template>

<style>
.imglogo {
  border-radius: 50%;
}


</style>