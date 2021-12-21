<template>
  <div>
      <footer class="w-full bg-black">
          <div class="max-w-7xl mx-auto flex flex-col sm:flex-row px-4 sm:px-6 lg:px-8 py-8 text-white">
              <div class="w-1/2">
                <!-- logo  -->
                <div class="flex items-center">
                  <nuxt-link class="flex-shrink-0 mb-4" to="/">
                    <!-- <img
                      class="w-24 object-fit"
                      src="~assets/images/VVVLogo.png"
                      alt="Valuable Varanus Vault logo"
                    > -->
                  </nuxt-link>
                </div>
                <!-- <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p> -->
              </div>
              <div class="w-full mt-12 md:mt-0 md:w-1/2 flex">
                <div class="w-full md:w-1/2">
                  <!-- <span class="text-vvv-primary text-xl">Socials</span>
                  <ul class="flex w-full"> -->
                    <!-- <li class="ml-1"><nuxt-link to="#" class="text-white hover:text-vvv-primary"><img src="~assets/images/twitter-brands.svg" alt="Twitter" class="text-vvv-cream w-1/3 h-auto"></nuxt-link></li>
                    <li class="ml-1"><nuxt-link to="#" class="text-white hover:text-vvv-primary"><img src="~assets/images/discord-brands.svg" alt="Discord" class="text-vvv-cream w-1/3 h-auto"></nuxt-link></li>
                    <li class="ml-1"><nuxt-link to="#" class="text-white hover:text-vvv-primary"><img src="~assets/images/instagram-brands.svg" alt="Instagram" class="text-vvv-cream w-1/3 h-auto"></nuxt-link></li> -->
                  <!-- </ul> -->
                </div>
                <div class="w-full md:w-1/2">
                  <span class="text-brand-primary text-xl">Quick Links</span>
                  <ul>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-vvv-primary">About</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-vvv-primary">Roadmap</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-vvv-primary">Community</nuxt-link></li>
                  </ul>
                </div>
              </div>
          </div>
          <div class="max-w-7xl mx-auto flex justify-between px-4 sm:px-6 lg:px-8 py-2 text-xs text-white border-t border-gray-400">
            <ul>
              <li>Terms & Conditions</li>
            </ul>
            <span class="text-center">© 2021 Co-box. All Rights Reserved.</span>
            <span class="text-right">Developed by <a href="https://verellino.com">Verellino</a>.</span>
          </div>
      </footer>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>