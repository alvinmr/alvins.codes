<template>
  <div class="mt-10 lg:mx-10">
    <nuxt-link class="px-4 py-2 text-white bg-black" to="/blog" exact>Back To Blog</nuxt-link>
    <Header :title="article.title" />

    <nuxt-content
      class="mx-auto mt-24 prose text-justify sm:prose lg:prose-lg xl:prose-xl"
      :document="article"
    />
  </div>
</template>

<script>
import Header from "~/components/Header.vue";
export default {
  components: { Header },
  head() {
    return {
      title: `alvinscodes | ${this.article.title}`,
      meta: [
        { hid: "og:title", name: "og:title", content: this.article.title },
        {
          hid: "og:image",
          name: "og:image",
          content: this.article.header_image,
        },
        {
          hid: "og:description",
          name: "og:description",
          content: this.article.description,
        },
        {
          hid: "description",
          name: "description",
          content: this.article.description,
        },
      ],
    };
  },
  async asyncData({ $content, params }) {
    const article = await $content("blog", params.slug).fetch();
    return { article };
  },
};
</script>

<style>
.prose h1,
.prose h2,
.prose h3,
.prose h4,
.prose h5 {
  @apply font-brandonBlack  text-black font-medium;
}

.prose p {
}
</style>