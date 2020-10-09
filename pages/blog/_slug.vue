<template>
  <div class="mt-10 lg:mx-10">
    <nuxt-link class="px-4 py-2 text-white bg-black" to="/blog" exact
      >Back To Blog</nuxt-link
    >
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
        {
          hid: "twitter:card",
          name: "twitter:card",
          content: "summary_large_image",
        },
        {
          hid: "twitter:url",
          name: "twitter:url",
          content: "https://alvins.codes",
        },
        {
          hid: "twitter:title",
          name: "twitter:title",
          content: this.article.title,
        },
        {
          hid: "twitter:description",
          name: "twitter:description",
          content: this.article.description,
        },
        {
          hid: "twitter:image",
          name: "twitter:image",
          content: this.article.header_image,
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

.prose img {
  margin: 0 auto;
}
</style>