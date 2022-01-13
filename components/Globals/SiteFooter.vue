<template>
  <div>
      <footer class="w-full bg-purple-900">
          <div class="max-w-7xl mx-auto flex flex-col sm:flex-row px-4 sm:px-6 lg:px-8 py-8 text-white">
              <div class="w-1/2">
                <!-- logo  -->
                <div class="flex flex-col items-start">
                  <nuxt-link class="flex-shrink-0 mb-4" to="/">
                    <img
                      class="w-24 object-fit"
                      src="~assets/images/coboxlogo.png"
                      alt="Cobix logo"
                    >
                  </nuxt-link>
                  <div class="text-sm">
                    <p>Reach out to our team:</p>
                    <p>E-mail: <a href="mailto:coboxvaccine.id@gmail.com">coboxvaccine.id@gmail.com</a></p>
                    <p>Whatsapp: +6287700553811</p>
                    <p>Phone: +6287700553811</p>
                    <p>Head: Green Hills Residence no 18, Jatihandap, Mandalajati, Kota Bandung</p>
                  </div>
                </div>
                <!-- <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p> -->
              </div>
              <div class="w-full mt-12 md:mt-0 md:w-1/2 flex flex-col md:flex-row">
                <div class="w-full md:w-1/2">
                  <span class="text-2xl">Quick Links</span>
                  <ul>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-brand-primary">Product</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-brand-primary">Market Target</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-brand-primary">About Us</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-brand-primary">Partnership</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-brand-primary">Business Schematic</nuxt-link></li>
                    <li class="mt-1"><nuxt-link to="#" class="text-white hover:text-brand-primary">Contact Us</nuxt-link></li>
                  </ul>
                </div>
                <div class="w-full md:w-1/2">
                  <span class="text-2xl">Socials</span>
                  <ul class="flex w-full mt-4">
                    <li class="">
                      <a href="#">
                        <img src="~assets/images/twitter-brands.svg" alt="Twitter" class="text-white hover:text-brand-primary w-8 h-8">
                        </a></li>
                    <li class="ml-12">
                      <a href="#">
                        <img src="~assets/images/instagram-brands.svg" alt="Instagram" class="text-white hover:text-brand-primary w-8 h-8">
                        </a></li>
                    <li class="ml-12">
                      <a href="#">
                        <img src="~assets/images/facebook-brands.svg" alt="Discord" class="text-white hover:text-brand-primary w-8 h-8">
                        </a></li>
                  </ul>
                </div>
              </div>
          </div>
          <div class="max-w-7xl mx-auto flex justify-between px-4 sm:px-6 lg:px-8 py-2 text-xs text-white border-t border-gray-400">
            <span class="text-left">© 2021 Co-box. All Rights Reserved.</span>
            <span class="text-right">Developed by <a href="https://verellino.com" class="">Verellino</a>.</span>
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