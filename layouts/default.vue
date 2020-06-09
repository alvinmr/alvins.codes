<template>
  <div class="container px-4">
    <nav>
      <div class="grid justify-center mt-4 text-center">
        <div>
          <div class="text-2xl tracking-widest font-brandonBlack">
            ALVIN'S
            <span class="opacity-50">CODES</span>
          </div>
        </div>
        <div class="my-4 text-sm tracking-wide uppercase nav-menu font-brandonBlack">
          <nuxt-link class="mx-5 hover:underline" to="/">Home</nuxt-link>
          <nuxt-link class="mx-5 hover:underline" to="/contact">Contact</nuxt-link>
        </div>
      </div>
    </nav>
    <nuxt />
    <footer class="grid justify-center mt-16 mb-4 text-center align-middle">
      <div class="text-2xl tracking-widest font-brandonBlack">
        ALVIN'S
        <span class="opacity-50">CODES</span>
      </div>
      <p class="text-xs opacity-50">hey feel free to reach me</p>
      <ul class="grid grid-flow-col gap-5 text-xs">
        <li>
          <a href="#">Instagram</a>
        </li>/
        <li>
          <a href="#">Email</a>
        </li>/
        <li>
          <a href="#">Github</a>
        </li>
      </ul>
    </footer>
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
  transition: 0.4s ease-in;
  @apply opacity-50;
}
</style>
