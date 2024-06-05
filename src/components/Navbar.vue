<template>
  <nav
    :class="{ 'bg-black  z-10 sticky top-0 transition-all duration-500 max-lg:bg-black': isScrolled, 'bg-transparent z-10 sticky top-0 transition-all duration-500 max-lg:bg-black': !isScrolled }">
    <div class=" bg-red-500 hidden max-lg:block">
      <img class="h-12" src="/navbar-logo.png" alt="">
    <img class="w-7 lg:hidden justify-self-end cursor-pointer" src="/mobile.png" alt="" x-on:click="isOpen = ! isOpen">
    <img class="h-6" src="/shopping-cart.png" alt="">
    <img class="h-6" src="/magnifying-glass.png" alt=""> 
    </div>

    <div class=" flex items-center space-x-3 justify-around py-5 max-lg:hidden">
      <img class="h-12" src="/navbar-logo.png" alt="">
      <ul class="flex space-x-10 text-white font-bold">
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="">HOME</a>
        </li>
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="#about">ABOUT US</a>
        </li>
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="#products">PRODUCTS</a>
        </li>
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="#call">CUSTOMERS</a>
        </li>
      </ul>
      <div class="flex space-x-3">
        <img class="h-6" src="/shopping-cart.png" alt="">
        <img class="h-6" src="/magnifying-glass.png" alt="">
      </div>
    </div>

    <div class="absolute top-20 left-0 z-10 bg-black w-full text-center" x-show="!isOpen">
      <ul class=" text-white font-bold">
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="">HOME</a>
        </li>
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="#about">ABOUT US</a>
        </li>
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="#products">PRODUCTS</a>
        </li>
        <li class="hover:bg-[#BC9667] py-2 px-3">
          <a href="#call">CUSTOMERS</a>
        </li>
      </ul>
      <div class="flex space-x-3">
        
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isOpen = ref(false);
function toggleMenu() {
  isOpen.value = !isOpen.value;
}

const isScrolled = ref(false);

function handleScroll() {
  if (window.scrollY > 0) {
    isScrolled.value = true;
  } else {
    isScrolled.value = false;
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>