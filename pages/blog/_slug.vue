<template>
  <div class="mt-10">
    <div class="flex items-center lg:ml-24">
      <nuxt-link
        class="px-4 py-2 text-sm text-white bg-black lg:w-auto"
        to="/blog"
        exact
      >
        <div class="flex flex-row items-center">
          <div>
            <svg
              width="20"
              height="20"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M21 12H3M3 12L10 5M3 12L10 19"
                stroke="#fff"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              ></path>
            </svg>
          </div>
          <div class="ml-5">back to article list</div>
        </div></nuxt-link
      >
    </div>
    <Header
      :title="article.title"
      :author="article.author"
      :date="$moment(article.createdAt).format('Do MMM YYYY')"
      :time_read="timeRead(article.readingTime)"
    />

    <nuxt-content
      class="mx-auto mt-24 prose sm:prose lg:prose-lg xl:prose-xl"
      :document="article"
    />
  </div>
</template>

<script>
import Header from "~/components/Header.vue";
export default {
  components: { Header },
  methods: {
    timeRead(milisecond) {
      return Math.floor(milisecond / 60000);
    },
  },
  head() {
    return {
      title: `alvinscodes | ${this.article.title}`,
      meta: [
        { hid: "og:title", name: "og:title", content: this.article.title },
        {
          hid: "og:image",
          name: "og:image",
          content: `https://serverless.alvinmr.vercel.app/og.jpg?author=${
            this.article.author
          }&website=alvins.codes&title=${
            this.article.title
          }&image=&date_time=${this.$moment(this.article.cratedAt).format(
            "Do MMM YYYY"
          )}`,
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
          content: `https://serverless.alvinmr.vercel.app/og.jpg?author=${
            this.article.author
          }&website=alvins.codes&title=${
            this.article.title
          }&image=&date_time=${this.$moment(this.article.cratedAt).format(
            "Do MMM YYYY"
          )}`,
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
.prose {
  color: black;
  max-width: none;
}

@screen lg {
  .prose {
    max-width: 80%;
  }
}

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