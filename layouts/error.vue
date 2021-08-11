<template>
  <div
    class="flex flex-col justify-center mt-48 mb-10 text-center align-middle"
  >
    <div v-if="error.statusCode === 404">
      <h1 class="text-6xl font-bold tracking-widest">404</h1>
      <h1>Page not found</h1>
    </div>
    <h1 v-else>An error occurred</h1>
    <nuxt-link
      exact
      to="/"
      class="w-64 px-2 py-2 mx-auto mt-2 text-white bg-black border-2 border-black"
      >Home page</nuxt-link
    >
  </div>
</template>

<script>
export default {
  props: ["error"],
};
</script>