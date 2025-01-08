<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isMenuOpen = ref(false);

function showMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}

function outsideClickHandler(event) {
  if (!event.target.closest("#menu") && !event.target.closest("#burger")) {
    isMenuOpen.value = false;
  }
}

onMounted(() => {
  window.addEventListener("click", outsideClickHandler);
});

onUnmounted(() => {
  window.removeEventListener("click", outsideClickHandler);
});
</script>

<template>
  <header>
    <div class="flex items-center justify-between bg-gray-800 p-7 text-white">
      <div class="btn">
        <div>Page Title</div>
      </div>
      <div class="">
        <div
          id="burger"
          @click="showMenu"
          class="col-span-1 cursor-pointer content-center justify-items-end px-4 md:hidden"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
            />
          </svg>
        </div>
        <nav class="hidden md:block">
          <ul class="flex space-x-4">
            <li
              v-for="(item, index) in ['Menu 1', 'Menu 2', 'Menu 3']"
              :key="item"
              class="btn"
            >
              <span>{{ item }}</span>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
  <nav
    id="menu"
    class="absolute right-0 transform transition-all duration-500 ease-in-out md:hidden"
    :class="[
      isMenuOpen
        ? 'pointer-events-auto translate-y-0 opacity-100'
        : 'pointer-events-none -translate-y-2 opacity-0',
    ]"
  >
    <ul class="rounded-b-md bg-gray-800 px-4 pb-5 text-white md:space-x-4">
      <li
        v-for="(item, index) in ['Menu 1', 'Menu 2', 'Menu 3']"
        :key="item"
        class="btn transition-all duration-300"
        :class="{ 'mt-4': index > 0 }"
        :style="{
          transform: isMenuOpen ? 'translateY(0)' : 'translateY(-10px)',
          opacity: isMenuOpen ? '1' : '0',
          transitionDelay: `${index * 100}ms`,
        }"
      >
        <span>{{ item }}</span>
      </li>
    </ul>
  </nav>
</template>
