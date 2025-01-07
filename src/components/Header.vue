<script setup>
function showMenu() {
  const menu = document.querySelector("#menu");
  if (!menu) {
    return;
  }

  if (menu.classList.contains("hidden")) {
    menu.classList.remove("hidden");
  } else {
    menu.classList.add("hidden");
  }
}
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
  <nav
    id="menu"
    class="absolute right-0 hidden overflow-clip rounded-b-md bg-gray-800 px-4 pb-4 text-white transition delay-150 ease-in-out md:space-x-4"
  >
    <ul>
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
</template>
