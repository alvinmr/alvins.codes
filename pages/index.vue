<template>
  <div class="container text-center">
    <navbar />
    <div class="hidden hello lg:block md:block">
      <p class="text-white opacity-50 font-brandon hello">HELLO</p>
    </div>
    <div class="container grid justify-center mt-32 lg:mt-40 md:mt-38">
      <p class="text-xs text-center lg:text-3xl lg:text-center md:text-3xl md:text-center">
        I'm a web developer based in
        <br />Bali - Indonesia who loves to
        <br />translate design into real think 💻🤘
      </p>
    </div>
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";

export default {
  components: {
    Navbar
  }
};
</script>

<style scoped>
.hello {
  position: absolute;
  top: 50%;
  left: 50%;
  z-index: -1;
  transform: translate(-50%, -50%);
  text-shadow: 6px 6px 3px #0000003b;
  font-size: 300px;
}
</style>
