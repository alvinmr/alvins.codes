<template>
  <div class="container px-4">
    <div class="grid justify-center mt-4 text-center">
      <div>
        <div class="text-2xl tracking-widest font-brandonBlack">
          ALVIN'S
          <span class="opacity-50">CODES</span>
        </div>
      </div>
      <div class="mt-4 text-sm tracking-wide uppercase nav-menu font-brandonBlack">
        <nuxt-link class="mx-5 hover:underline" to="/">Home</nuxt-link>
        <nuxt-link class="mx-5 hover:underline" to="/contact">Contact</nuxt-link>
        <nuxt-link class="mx-5 hover:underline" to="/blog">Blog</nuxt-link>
      </div>
    </div>
    <nuxt />
  </div>
</template>


<style>
@font-face {
  font-family: "Brandon";
  src: url("~assets/fonts/Brandon_reg.otf");
}

@font-face {
  font-family: "Brandon Black";
  src: url("~assets/fonts/Brandon_blk.otf");
}

::-webkit-scrollbar {
  display: none;
}

body {
  font-family: "DM Mono";
  background-color: #f6f6f6;
}

.active-link {
  @apply opacity-50;
}
</style>
