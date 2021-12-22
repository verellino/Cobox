<template>
  <div>
    <main>
      <div class="mt-16">
        <!-- Hero Section  -->
      <div class="w-full bg-right sm:bg-center bg-no-repeat bg-cover py-8 md:py-40" :style="{ backgroundImage: `url(${backgroundImage})`}">
      
        <div class="hero max-w-7xl mx-auto flex flex-col sm:flex-row md:py-30 py-8 px-4 md:px-8">
          <div class="w-full sm:w-1/2 py-6 sm:px-0">
            <h1>Co-Box Vaccine Carrier</h1>
            <p>Distribute the vaccine to overcome the pandemic!</p>
            <a href="#product" class="my-8 inline-block rounded-md text-white py-3 px-8 bg-brand-primary btn-brand">
              <span>Discover more</span>
            </a>
          </div>
          <div class="w-full sm:w-1/2 my-5">
            <!-- <img src="~assets/images/VVVLogo.png" alt="Valuable Varanus Vault" class="w-60"> -->
          </div>
        </div>
      </div>

      <!-- Product Section  -->
      <div id="product" class="max-w-7xl mx-auto py-12 md:py-20 px-4 md:px-8">
        <div class="py-6 flex flex-col sm:flex-row justify-center items-center">
          <div class="w-full md:w-1/2 flex justify-center items-center">
            <div class="h-40 w-40 sm:h-96 sm:w-96 flex justify-center items-center">
              <img src="~assets/images/cobox1.jpg" alt="Cobox" class="block m-auto">
            </div>
          </div>
          <div class="w-full md:w-1/2">
            <h2 class="text-brand-primary">Co-Box Vaccine Carrier</h2>
            <p>A modified conventional vaccine carrier with temperature control and monitoring system with shockproof outerbox material, that can keep the vaccine safe and maintain vaccine quality during the distribution process</p>
          </div>
        </div>
      </div>
      
      <!-- Our Solution Section  -->
      <div id="ourSolution" class="max-w-7xl mx-auto py-12 md:py-20 px-4 md:px-8">
        <div class="py-6 flex flex-col sm:flex-row justify-center items-center">
          <div class="w-full md:w-1/2">
            <h2 class="text-brand-primary">Our Solution</h2>
            <p>Portable and hand-held vaccine carrier with maximum capacity 5 liter and maximum weight 8kg</p>
          </div>
          <div class="w-full md:w-1/2">
            <div class="flex justify-center items-center">
              <div class="w-full h-auto mt-12 sm:h-96 sm:w-96 flex justify-center items-center">
                <img src="~assets/images/cobox2.jpg" alt="Cobox" class="block m-auto">
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Market Target Section  -->
      <div id="marketTarget" class="w-full py-12 md:py-20 px-4 md:px-8 bg-brand-primary text-white">
        <h2 class="text-center text-white mb-12">Market Target</h2>
        <div class="max-w-7xl mx-auto py-8 grid grid-cols-1 sm:grid-cols-3">
          <div class="text-center sm:border-r border-white py-6 px-4"><h3 class="text-white">23.476</h3><span>RS & Puskesmas di Indonesia</span></div>
          <div class="text-center sm:border-r border-white py-6 px-4"><h3 class="text-white">2.613</h3><span>RS & Puskesmas di Jawa Barat</span></div>
          <div class="text-center py-6 px-4"><h3 class="text-white">172</h3><span>RS & Puskesmas di Bandung dan Kabupaten Bandung</span></div>
        </div>
      </div>

      <!-- About Us Section  -->
      <div id="aboutUs" class="max-w-7xl mx-auto py-12 md:py-20 px-4 md:px-8">
        <div class="py-6 flex flex-col justify-center items-center">
          <h2>About Us</h2>
          <p class="w-full">Co-Box merupakan vaccine carrier dengan sistem pendinginan menggunakan termoelektrik yang terintegrasi dengan sistem monitoring dan kontrol temperatur sehingga dapat menjaga temperatur vaksin secara konsisten dibandingkan vaccine carrier konvensional yang hanya menggunakan ice pack. Visi kami membantu penanganan pandemi COVID-19 dan pemerataan vaksinasi bagi masyarakat Indonesia melalui proses distribusi vaksin yang aman dan nyaman, dengan misi menyediakan vaccine carrier dengan fitur-fitur yang mempermudah dan menjamin terlaksana nya rantai-dingin vaksin yang aman dengan kualitas vaksin yang terjaga.</p>
          <div class="aboutus-img w-full rounded-2xl overflow-hidden mt-16">
            <img src="~assets/images/cobox3.jpg" alt="Cobox" class="w-full block m-auto">
          </div>
        </div>
      </div>

      <!-- Partnership Opportunity Section  -->
      <div id="partnership" class="w-full mx-auto py-12 md:py-20 px-4 md:px-8 bg-blue-300">
        <div class="max-w-7xl mx-auto py-6 flex flex-col sm:flex-row justify-center items-center">
          <div class="w-full sm:w-1/2">
            <h2 class="text-brand-secondary">Partnership opportunity</h2>
            <p>Bersama kami, kembangkan koneksi antar Anda sebagai perusahaan farmasi, rumah sakit, puskesmas, maupun instansi kesehatan lain dalam pengadaan vaksinasi COVID-19 sembari membantu pemerataan program vaksinasi COVID-19 di Indonesia khususnya ke daerah pelosok 3T</p>
            <nuxt-link to="/about" class="my-8 inline-block rounded-md text-white py-3 px-8 bg-brand-primary btn-brand">
              <span>Become our partner</span>
            </nuxt-link>
          </div>
          <div class="w-full sm:w-1/2">
            <div class="h-40 w-40 sm:h-96 sm:w-96 mx-auto flex justify-center items-center">
              <img src="~assets/images/team_up.svg" alt="Cobox" class="w-full block m-auto">
            </div>
          </div>
        </div>
      </div>

      <!-- Contact UsSection  -->
      <div id="contactUs" class="max-w-7xl mx-auto py-12 md:py-20 px-4 md:px-8">
        <div class="py-6 flex flex-col justify-center items-center">
          <h2>Reach out to our team</h2>

          <div v-if="success" class="rounded bg-indigo-500 text-white text-lg p-4">
          Great! Your message has been sent successfully. I will try to respond
          quickly.
        </div>
        <form v-else class="w-full max-w-7xl mt-16" v-on:submit.prevent="sendMessage">
            <div class="flex flex-wrap -mx-3 mb-6">
              <div v-if="errored" class="rounded bg-red-200 text-lg p-4">
                Bummer, Something went wrong. Did you fill out all of the fields?
              </div>
              <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-first-name">
                  Your Name
                </label>
                <input class="appearance-none block w-full bg-gray-200 text-gray-700 border rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white" 
                required v-model="name" id="grid-first-name" type="text" placeholder="Joko Widodo">
                <!-- <p class="text-red-500 text-xs italic">Please fill out this field.</p> -->
              </div>
              <div class="w-full md:w-1/3 px-3 mb-6">
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-email">
                  Your Email
                </label>
                <input class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" 
                required v-model="email" id="grid-email" type="email" placeholder="nama@email.com">
              </div>
              <div class="w-full md:w-1/3 px-3 mb-6">
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-phone">
                  Whatsapp Contact
                </label>
                <input class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" 
                required v-model="phone" id="grid-phone" type="phone" placeholder="081.....90">
              </div>
              <div class="w-full px-3 mb-6">
                <label class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-phone">
                  Your Message
                </label>
                <textarea class="appearance-none block w-full h-24 bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500" 
                required v-model="message" id="grid-message" type="text" placeholder="Your message..."></textarea>
              </div>
              <div class="mt-4 w-full">
                <div class="w-1/2 mx-auto">
                  <button class="shadow w-full mx-auto bg-purple-500 hover:bg-purple-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded btn-brand" type="submit">
                  {{ loading ? "Sending Message..." : "Submit" }}
                  </button>
                </div>
              </div>
            </div>
          </form>

        </div>
      </div>
      

      </div>
    </main>
  </div>
</template>

<script>
import backgroundImage from '~/assets/images/HeroBg.png'
export default {
  data() {
    return { 
      backgroundImage,
      loading: false,
      success: false,
      errored: false,
      name: "",
      email: "",
      phone: "",
      message: "",
      }
  },
  methods: {
    sendMessage() {
      this.loading = true;
      this.$axios
        .post("/messages", {
          name: this.name,
          email: this.email,
          phone: this.phone,
          message: this.message,
        }).then(response => {
          this.success = true
          this.errored =false
        })
        .catch(error => {
          this.errored = true
        })
        .finally(() => {
          this.loading = false
        });
    },
  }
}
</script>

<style scoped>
@media (min-width: 456px) {
  .aboutus-img {
    height: 420px;
  }
}
</style>