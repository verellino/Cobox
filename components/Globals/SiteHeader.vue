<template>
  <div>
    <nav class="bg-white fixed w-full z-50 top-0 drop-shadow-xl">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-16">
          <!-- Logo -->
          <div class="flex items-center">
            <nuxt-link class="flex-shrink-0" to="/">
              <!-- <img
                class="w-20 object-fit"
                src="~assets/images/VVVLogo.png"
                alt="Valuable Varanus Vault logo"
              > -->
            </nuxt-link>
          </div>
          <!-- Right nav -->
          <div class="hidden md:block">
            <div class="ml-10 flex items-center">
                <nuxt-link
                  to="/"
                  class="px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-brand-primary focus:text-white focus:bg-purple-700"
                >Home</nuxt-link>
                
                <a
                  href="#product"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
                >Product</a>
                <a
                  href="#marketTarget"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
                >Market Target</a>
                <a
                  href="#aboutUs"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
                >About Us</a>
                <a
                  href="#partnership"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
                >Partnership</a>
                <nuxt-link
                  to="/about"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
                >Business Schematic</nuxt-link>
                <a
                  href="#contactUs"
                  class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
                >Contact Us</a>
              </div>
          </div>
          <div class="-mr-2 flex md:hidden">
            <!-- Mobile menu button -->
            <button
              class="inline-flex items-center justify-center p-2 rounded-md text-gray-900 hover:text-white hover:bg-purple-700 focus:outline-none focus:bg-purple-700 active:text-red focus:text-white"
              @click="toggle"
            >
              <svg
                :class="[isOpen ? 'hidden' : 'block', 'h-6 w-6']"
                stroke="currentColor"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                ></path>
              </svg>
              <svg
                :class="[isOpen ? 'block' : 'hidden', 'h-6 w-6']"
                stroke="currentColor"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                ></path>
              </svg>
            </button>
          </div>
        </div>
      </div>
      <div :class="[isOpen ? '' : 'hidden', 'md:hidden']">
        <div class="px-2 pt-2 pb-3 sm:px-3">
          <nuxt-link
            to="/"
            class="px-3 py-2 block rounded-md font-medium text-red focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >Home</nuxt-link>
          
          <a
            href="#product"
            class="px-3 py-2 block rounded-md font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >Product</a>
          <a
            href="#marketTarget"
            class="px-3 py-2 block rounded-md font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >Market Target</a>
          <a
            href="#aboutUs"
            class="px-3 py-2 block rounded-md font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >About Us</a>
          <a
            href="#partnership"
            class="px-3 py-2 block rounded-md font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >Partnership</a>
          <nuxt-link
            to="/about"
            class="px-3 py-2 block rounded-md font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >Business Schematic</nuxt-link>
          <a
            href="#contactUs"
            class="px-3 py-2 block rounded-md font-medium text-gray-900 hover:text-purple-800 focus:outline-none active:text-red focus:text-white focus:bg-purple-700"
          >Contact Us</a>
        </div>
      </div>
    </nav> 
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    toggle () {
      this.isOpen = !this.isOpen
    }
  }
}
</script>