<template>
  <div>
    <div class="grid grid-flow-row lg:grid-flow-col">
      <div class="grid justify-center mt-4 text-center lg:text-left">
        <p class="text-xs font-black tracking-widest opacity-50 font-brandon">CONTACT</p>
        <h1 class="text-3xl lg:text-6xl font-brandonBlack">
          Let's work
          <br />together
        </h1>
        <img
          src="~assets/images/cont2.gif"
          class="w-2/3 mx-auto lg:w-full lg:mx-px"
          alt="contact me"
        />
      </div>
      <div class="p-3 mt-10 bg-white border-2 border-black lg:w-3/4 project-wrap">
        <div class="form-group">
          <label for="name">Your Name</label>
          <input class="input-group" type="text" name="name" />
        </div>
        <div class="form-group">
          <label for="email">Your Email</label>
          <input class="input-group" type="email" name="name" />
        </div>
        <div class="form-group">
          <label for="service">Service</label>
          <select class="input-group" name="service">
            <option value="hello">Just want say hello!</option>
            <option value="project">Need help with a project</option>
            <option value="longterm">Long term partnership</option>
            <option value="fulltime">Hire me full-time</option>
          </select>
        </div>
        <div class="form-group">
          <label for="message">Your Message</label>
          <textarea class="input-group" name="message"></textarea>
        </div>
        <button class="mt-3 btn-submit lg:w-32">SUBMIT</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  head() {
    return {
      title: "alvinscodes | contact"
    };
  }
};
</script>

<style>
.form-group {
  @apply mt-3;
}
.input-group {
  /* purgecss start ignore */
  @apply w-full border border-black bg-white py-1 px-2;
  /* purgecss end ignore */
}

.input-group:focus {
  @apply outline-none;
}

.btn-submit {
  @apply py-2 px-4 bg-black text-white text-center mb-5;
}
</style>