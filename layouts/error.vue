<template>
  <div class="grid justify-center mt-56 text-center">
    <h1 v-if="error.statusCode === 404">Page not found</h1>
    <h1 v-else>An error occurred</h1>
    <nuxt-link to="/" class="px-2 py-2 mt-2 text-white bg-black border-2 border-black">Home page</nuxt-link>
  </div>
</template>

<script>
export default {
  props: ["error"],
  layout: "blog" // Anda dapat mengatur layout kustom untuk halaman kesalahan
};
</script>