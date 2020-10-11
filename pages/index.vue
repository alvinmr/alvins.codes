<template>
  <div>
    <div class="text-center h-vh">
      <div class="grid justify-center align-middle">
        <p
          class="hidden text-white opacity-50 hello lg:block md:block font-brandonBlack"
        >
          HELLO
        </p>
        <p
          class="block mt-20 text-sm font-bold text-center lg:-mt-64 lg:text-3xl lg:text-center md:text-3xl md:text-center md:-mt-56"
        >
          Im a guy that can code and lil bit design, <br />
          but internet makes me can do anything.
        </p>
      </div>
    </div>
    <div class="grid mt-20 lg:mt-40 project">
      <p class="text-xs font-black tracking-widest opacity-50 font-brandon">
        PROJECT
      </p>
      <h1 class="text-xl lg:text-2xl font-brandonBlack">Recent Projects</h1>
      <div class="grid grid-cols-1 gap-5 mt-10 lg:gap-6 lg:grid-cols-2">
        <project
          :project="{
            title: 'ABELL',
            desc: 'Automatic Bell System',
            img: 'abell@2x.png',
            link: 'https://github.com/alvinmr/abell',
          }"
          style="background-color: #007bff"
        />
        <project
          :project="{
            title: 'SIPASTI',
            desc: 'Payment System For School',
            img: 'sipasti@2x.png',
            link: 'https://github.com/alvinmr/sipasti',
          }"
          style="background-color: #665dd3"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Project from "~/components/Project.vue";
export default {
  components: { Project },
};
</script>

<style scoped>
.hello {
  z-index: -1;
  text-shadow: 6px 6px 3px #0000003b;
  font-size: 300px;
}

@media only screen and (max-width: 768px) {
  .hello {
    font-size: 200px;
  }
}
</style>
