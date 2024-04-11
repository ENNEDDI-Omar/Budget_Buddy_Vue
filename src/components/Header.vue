<template>
  <h2></h2>

  <nav class="flex flex-wrap items-center justify-between p-4 bg-white">
    <div class="w-auto lg:order-2 lg:w-1/5 lg:text-center">
      <a class="text-xl font-semibold text-gray-800 font-heading" href="#">
        Expense Tracker
      </a>
    </div>
    <div class="block lg:hidden">
      <button
        class="flex items-center px-3 py-2 text-indigo-500 border border-indigo-500 rounded navbar-burger"
      >
        <svg
          class="w-3 h-3 fill-current"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
        </svg>
      </button>
    </div>
    <div class="hidden w-full navbar-menu lg:order-1 lg:block lg:w-2/5">
      <a
        class="block mt-4 mr-10 text-blue-900 lg:inline-block lg:mt-0 hover:text-indigo-600"
        href="#"
      >
        Home
      </a>
      <a
        class="block mt-4 mr-10 text-blue-900 lg:inline-block lg:mt-0 hover:text-indigo-600"
        href="#"
      >
        Expense
      </a>
      <a
        class="block mt-4 text-blue-900 lg:inline-block lg:mt-0 hover:text-indigo-600"
        href="#"
      >
        Galery
      </a>
    </div>
    <div
      class="hidden w-full navbar-menu lg:order-3 lg:block lg:w-2/5 lg:text-right">
      <div class="relative flex items-center w-full h-full lg:w-64 group">
            <div
              class="absolute z-50 flex items-center justify-center block w-auto h-10 p-3 pr-2 text-sm text-gray-500 uppercase cursor-pointer sm:hidden"
            >
              <svg
                fill="none"
                class="relative w-5 h-5"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"
                ></path>
              </svg>
            </div>
            <svg
              class="absolute left-0 z-20 hidden w-4 h-4 ml-4 text-gray-500 pointer-events-none fill-current group-hover:text-gray-400 sm:block"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
            >
              <path
                d="M12.9 14.32a8 8 0 1 1 1.41-1.41l5.35 5.33-1.42 1.42-5.33-5.34zM8 14A6 6 0 1 0 8 2a6 6 0 0 0 0 12z"
              ></path>
            </svg>
            <input
              type="text"
              class="block w-full py-1.5 pl-10 pr-4 leading-normal rounded-2xl focus:border-transparent focus:outline-none focus:ring-2 focus:ring-blue-500 ring-opacity-90 bg-gray-100 dark:bg-gray-800 text-gray-400 aa-input"
              placeholder="Search"
            />
            <div
              class="absolute right-0 hidden h-auto px-2 py-1 mr-2 text-xs text-gray-400 border border-gray-300 rounded-2xl md:block"
            >
              +
            </div>
          </div>
        <div
          class="relative flex items-center justify-end w-1/4 p-1 ml-5 mr-4 sm:mr-0 sm:right-auto">
          <a href="#" class="relative block">
            <img
            alt="profil"
            src="/images/person/1.jpg"
            class="mx-auto object-cover rounded-full h-10 w-10"
            />
          </a>
        </div>
    </div>
  </nav>

  
</template>
