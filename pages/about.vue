<template>
  <div>
    <main>
      <div class="mt-16">
        <!-- Hero Section  -->
      <div class="w-full bg-center bg-no-repeat bg-cover" :style="{ backgroundImage: `url(${partnerBg})`}">
      
        <div class="hero max-w-7xl mx-auto md:py-30 py-12 px-4 lg:px-8">
          <div class="w-full my-5 flex items-center justify-center bg-gray-300">
            <!-- <img src="~assets/images/VVVLogo.png" alt="Valuable Varanus Vault" class="w-60"> -->
          </div>
          <div class="py-6 sm:px-0">
            <h1>Partnership Opportunity</h1>
            <p>Bersama kami, kembangkan koneksi antar Anda sebagai perusahaan farmasi, rumah sakit, puskesmas, maupun instansi kesehatan lain dalam pengadaan vaksinasi COVID-19 sembari membantu pemerataan program vaksinasi COVID-19 di Indonesia khususnya ke daerah pelosok 3T</p>
            <a href="#partnerForm" class="my-8 inline-block rounded-md text-white py-3 px-8 bg-brand-primary btn-brand">
              <span>Become our partner</span>
            </a>
          </div>
        </div>
      </div>

      <!-- Business Schematic Section  -->
      <div id="businessSchematic" class="w-full py-20 px-4 lg:px-8 md:bg-center bg-no-repeat bg-cover" :style="{ backgroundImage: `url(${bizBg})`}">
        <div class="max-w-7xl mx-auto py-6 flex flex-col sm:flex-row justify-center items-center">
          <div class="w-full md:w-1/2">
            <h2 class="text-brand-primary">Business Schematic</h2>
            <p>Sebagai penyedia vaccine carrier dengan berbagai inovasi fitur yang kami kembangkan, kami menjalankan partnership B2B dengan perusahaan farmasi, rumah sakit, instansi kesehatan maupun instansi lain yang akan melakukan pengadaan vaksinasi COVID-19. </p>
          </div>
          <div class="w-full md:w-1/2">
            <div class="flex justify-center items-center">
              <div class="w-full h-auto mt-12 flex justify-center items-center">
                <img src="~assets/images/cobox.jpg" alt="Cobox" class="shadow block m-auto rounded-xl">
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Partner Form Section  -->
      <div id="partnerForm" class="max-w-7xl mx-auto py-20 px-4 lg:px-8">
        <div class="py-6 flex flex-col justify-center items-center">
          <h2>Reach out to our team</h2>
        </div>
        <div v-if="success" class="rounded bg-indigo-500 text-white text-lg p-4">
          Great! Your message has been sent successfully. I will try to respond
          quickly.
        </div>
        <form 
        v-else 
        class="w-full max-w-7xl mt-16" 
        v-on:submit.prevent="sendMessage" 
        method="post"
        data-netlify="true"
        data-netlify-honeypot="bot-field" 
        name="partner-form">
            <input type="hidden" name="partner-form" value="ask-question" />
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
                <div class="md:w-1/3"></div>
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
    </main>
  </div>
</template>

<script>
import partnerBg from '~/assets/images/PartnerBg.png'
import bizBg from '~/assets/images/9.png'
// import bizBg from '~/assets/images/9.png'
export default {
  data() {
    return { 
      partnerBg, 
      bizBg,
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

</style>