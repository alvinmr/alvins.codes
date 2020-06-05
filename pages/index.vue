<template>
  <div>
    <div class="text-center h-100 w-100">
      <div class="hidden hello lg:block md:block">
        <p class="text-white opacity-50 font-brandonBlack">HELLO</p>
      </div>
      <div class="grid justify-center mt-32 lg:mt-40 md:mt-38">
        <p
          class="text-sm font-bold text-center lg:text-3xl lg:text-center md:text-3xl md:text-center"
        >
          I'm a web developer based in
          <br />Bali - Indonesia who loves to
          <br />translate design into real stuffs 💻🤘
        </p>
      </div>
    </div>
    <div class="grid mt-56 project">
      <p class="text-xs font-black tracking-widest opacity-50 font-brandon">PROJECT</p>
      <h1 class="text-xl lg:text-2xl font-brandonBlack">Recent Projects</h1>
      <project />
      <project />
    </div>
  </div>
</template>

<script>
import Project from "~/components/Project.vue";
export default {
  components: { Project }
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

@media only screen and (max-width: 768px) {
  .hello {
    font-size: 200px;
  }
}
</style>
