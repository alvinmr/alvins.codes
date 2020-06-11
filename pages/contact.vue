<template>
  <div>
    <div v-if="loading">
      <div class="absolute top-0 left-0 z-10 w-screen h-screen bg-white">
        <img src="~assets/images/loading.gif" class="mx-auto mt-56" />
        <p class="mt-10 text-xl tracking-widest text-center">LOADING</p>
      </div>
    </div>

    <div v-else class="grid grid-flow-row lg:grid-flow-col">
      <div class="grid justify-center mt-4 text-center lg:text-left">
        <h1 class="w-full text-3xl lg:w-2/3 lg:text-6xl font-brandonBlack">Let's work together</h1>
        <img src="~assets/images/cont2.gif" class="mx-auto lg:mx-px" alt="contact me" />
      </div>
      <div
        class="p-3 mt-10 bg-white border-2 border-black lg:w-3/4 project-wrap shadow-theme rounded-theme"
      >
        <div class="text-red-700">
          <ul class="list-disc list-inside">
            <li v-for="error in errors" :key="error.id">{{ error }}</li>
          </ul>
        </div>
        <div class="form-group">
          <label for="name">Your Name</label>
          <input v-model="name" class="input-group" type="text" />
        </div>
        <div class="form-group">
          <label for="email">Your Email</label>
          <input v-model="email" class="input-group" type="email" />
        </div>
        <div class="form-group">
          <label for="service">Service</label>
          <select v-model="service" class="input-group" name="service">
            <option value disabled>Choose whats you needed</option>
            <option value="Just want say hello!">Just want say hello!</option>
            <option value="Need help with a project">Need help with a project</option>
            <option value="Long term partnership">Long term partnership</option>
            <option value="Hire me full-time">Hire me full-time</option>
          </select>
        </div>
        <div class="form-group">
          <label for="message">Your Message</label>
          <textarea class="input-group" v-model="message" name="message"></textarea>
        </div>
        <button class="mt-3 btn-submit lg:w-32" @click="sendEmail()">SUBMIT</button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  components: {},
  head() {
    return {
      title: "alvinscodes | contact"
    };
  },
  data() {
    return {
      errors: [],
      loading: false,
      name: "",
      email: "",
      service: "",
      message: ""
    };
  },
  methods: {
    sendEmail() {
      this.errors = [];
      if (!this.name) this.errors.push("Please fill your name ☹️");
      if (this.email.length < 20) this.errors.push("Fill the right email");
      if (!this.service) this.errors.push("Hmmm fill what service you want");
      if (!this.message) this.errors.push("Dont be shy! fill your message ☺️");
      else if (this.name && this.service && this.message) {
        axios({
          method: "post",
          url: `https://api.telegram.org/bot${process.env.BOT_TELE_API}/sendMessage`,
          data: {
            text: `New message from alvins.codes! \nFrom : ${this.name}\nEmail : ${this.email}\nService : ${this.service}\nMessage : ${this.message}`,
            chat_id: "469848777"
          }
        })
          .then(res => {
            this.$router.replace("/success");
          })
          .catch(err => {
            console.log(err);
          });
      }
    },
    start() {
      this.loading = true;
    },
    finish() {
      this.loading = false;
    }
  }
};
</script>

<style>
.form-group {
  @apply mt-3;
}
.input-group {
  @apply w-full border border-black bg-white py-1 px-2;
}

.input-group:focus {
  @apply outline-none;
}

.btn-submit {
  @apply py-2 px-4 bg-black text-white text-center mb-5;
}
</style>
