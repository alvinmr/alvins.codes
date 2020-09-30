<template>
  <figure>
    <img :src="`${src}`" :alt="`${alt}`" />
    <figcaption class="text-center">{{ caption }}</figcaption>
  </figure>
</template>

<script>
export default {
  name: "image-with-capt",
  props: {
    src: String,
    alt: String,
    caption: String,
  },
};
</script>

<style>
</style>