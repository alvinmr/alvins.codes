<template>
  <transition name="page">
    <div class="container px-4">
      <nav>
        <div class="flex flex-col items-center mt-4 text-center lg:flex-row lg:justify-between">
          <div>
            <div class="text-2xl tracking-widest font-brandonBlack">
              ALVIN'S
              <span class="opacity-50">CODES</span>
            </div>
          </div>
          <div class="my-4 text-sm tracking-wide uppercase nav-menu font-brandonBlack">
            <nuxt-link class="mx-5 hover:underline" to="/" exact>Home</nuxt-link>
            <nuxt-link class="mx-5 hover:underline" to="/blog">Blog</nuxt-link>
            <nuxt-link class="mx-5 hover:underline" to="/contact" exact>Contact</nuxt-link>
          </div>
        </div>
      </nav>
      <nuxt />
      <footer class="grid justify-center mt-16 mb-4 text-center align-middle">
        <div class="text-2xl tracking-widest font-brandonBlack">
          ALVIN'S
          <span class="opacity-50">CODES</span>
        </div>
        <p class="text-xs opacity-50">hey hit me up!</p>
        <ul class="grid grid-flow-col gap-5 text-xs">
          <li>
            <a href="https://instagram.com/aaaaaaaaaaaalvin">Instagram</a>
          </li>/
          <li>
            <a href="mailto:maulanaalvin1@gmail.com">Email</a>
          </li>/
          <li>
            <a href="https://github.com/alvinmr">Github</a>
          </li>
        </ul>
      </footer>
    </div>
  </transition>
</template>


<style >
.page-enter-active,
.page-leave-active {
  transition: opacity 0.5s;
}

.page-enter,
.page-leave-active {
  opacity: 0;
}

@font-face {
  font-family: "Brandon";
  src: url("~assets/fonts/Brandon_reg.otf");
}

@font-face {
  font-family: "Brandon Black";
  src: url("~assets/fonts/Brandon_blk.otf");
}

/* ::-webkit-scrollbar {
  display: none;
} */

body {
  font-family: "DM Mono";
  background-color: #f6f6f6;
  transition: 1s ease-in;
  /* -ms-overflow-style: none; */
}

.active-link {
  transition: 0.4s ease-in;
  @apply opacity-50;
}
</style>
