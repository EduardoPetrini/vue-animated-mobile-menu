<script setup>
function showMenu() {
  const menu = document.querySelector('#menu');
  if (!menu) {
    return;
  }
  
  if (menu.classList.contains('hidden')) {
    menu.classList.remove('hidden');
  } else {
    menu.classList.add('hidden');
  }
}
</script>

<template>
  <header>
    <div class="flex justify-between items-center bg-gray-800 text-white p-7">
      <div class="btn">
        <div>Page Title</div>
      </div>
      <div class="">
        <div id="burger" @click="showMenu" class="px-4 cursor-pointer md:hidden col-span-1 content-center justify-items-end">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
          </svg>
        </div>
        <nav>
          <ul id="menu" class="md:flex md:space-x-4 hidden mt-5">
            <li class="btn mt-3">
              <span>Menu 1</span>
            </li>
            <li class="btn mt-3">
              <span>Menu 2</span>
            </li>
            <li class="btn mt-3">
              <span>Menu 3</span>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

