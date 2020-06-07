<template>
  <div class="w-full mt-5 border-2 border-black rounded-md lg:mt-10">
    <div class="relative grid text-white font-brandonBlack project-wrap">
      <div class="flex flex-row justify-between mx-4 mt-4 text-md lg:text-xl">
        <p>2020</p>
        <a class="tracking-wider" href="#">
          View Project
          <svg class="inline w-5 svg-icon" viewBox="0 0 20 20">
            <path
              fill="#fff"
              d="M1.729,9.212h14.656l-4.184-4.184c-0.307-0.306-0.307-0.801,0-1.107c0.305-0.306,0.801-0.306,1.106,0
              l5.481,5.482c0.018,0.014,0.037,0.019,0.053,0.034c0.181,0.181,0.242,0.425,0.209,0.66c-0.004,0.038-0.012,0.071-0.021,0.109
              c-0.028,0.098-0.075,0.188-0.143,0.271c-0.021,0.026-0.021,0.061-0.045,0.085c-0.015,0.016-0.034,0.02-0.051,0.033l-5.483,5.483
              c-0.306,0.307-0.802,0.307-1.106,0c-0.307-0.305-0.307-0.801,0-1.105l4.184-4.185H1.729c-0.436,0-0.788-0.353-0.788-0.788
              S1.293,9.212,1.729,9.212z"
            />
          </svg>
        </a>
      </div>
      <div class="flex flex-col justify-center my-5 text-center title">
        <h1 class="text-2xl tracking-wider lg:text-6xl font-brandonBlack">{{ project.title }}</h1>
        <h3 class="text-base tracking-wide lg:text-3xl font-brandonBlack">{{ project.desc }}</h3>
      </div>
      <div class="flex justify-center">
        <img class="w-5/6" :src="require(`@/assets/images/${project.img}`)" alt />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["project"]
};
</script>

<style>
.view-btn {
  right: 0;
}
.project-wrap {
  box-shadow: 12px 12px 0px #1b262c;
  @apply rounded-md;
}
</style>