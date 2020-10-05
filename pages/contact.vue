<template>
  <div>
    <div class="grid grid-flow-row lg:grid-flow-col">
      <div class="grid justify-center mt-4 text-center h-80 lg:text-left">
        <h1
          class="w-full text-3xl lg:w-2/3 lg:text-6xl md:text-6xl font-brandonBlack"
        >Let's work together</h1>
        <img src="~assets/images/cont2.gif" class="mx-auto lg:mx-px" alt="contact me" />
      </div>
      <div
        class="p-3 mt-10 bg-white border-2 border-black lg:w-3/4 project-wrap shadow-theme rounded-theme"
      >
        <form v-on:submit.prevent="sendEmail">
          <div class="text-red-700">
            <ul class="list-disc list-inside error">
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
              <option value disabled>Choose what you needed</option>
              <option value="Just wanna say hello!">Just wanna say hello!</option>
              <option value="Need help with a project">Need help with a project</option>
              <option value="Long term partnership">Long term partnership</option>
              <option value="Hire me full-time">Hire me full-time</option>
            </select>
          </div>
          <div class="form-group">
            <label for="message">Your Message</label>
            <textarea class="input-group" v-model="message" name="message"></textarea>
          </div>
          <button type="submit" class="mt-3 btn-submit lg:w-32">SUBMIT</button>
        </form>
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
      title: "alvinscodes | contact",
    };
  },
  data() {
    return {
      errors: [],
      name: "",
      email: "",
      service: "",
      message: "",
    };
  },
  methods: {
    sendEmail() {
      this.errors = [];
      if (!this.name) this.errors.push("Please fill your name ☹️");
      if (!this.service) this.errors.push("Hmmm fill what service you want");
      if (!this.message) this.errors.push("Dont be shy! fill your message ☺️");
      else if (this.name && this.service && this.message) {
        axios({
          method: "post",
          url: `https://api.telegram.org/bot${process.env.BOT_TELE_API}/sendMessage`,
          data: {
            text: `New message from alvins.codes! \nFrom : ${this.name}\nEmail : ${this.email}\nService : ${this.service}\nMessage : ${this.message}`,
            chat_id: "469848777",
          },
        })
          .then((res) => {
            this.$router.replace("/success");
          })
          .catch((err) => {
            console.log(err);
          });
      }
    },
  },
};
</script>

<style scoped>
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.error {
  animation: fadeIn 1s;
}
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
