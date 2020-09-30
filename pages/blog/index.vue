<template>
  <div>
    <Header
      hasDescription
      title="Blog."
      desc="This is my blog where I can think out loud. This blog will be place for me to sharing or note about anything "
    />
    <div class="flex mt-40">
      <h1 class="text-3xl lg:text-4xl font-brandonBlack">My Articles</h1>
    </div>
    <div class="grid grid-cols-1 gap-16 mt-8 lg:grid-flow-row lg:grid-cols-3">
      <div v-for="blog in blogs" :key="blog.slug">
        <Article
          :article="{
            title: blog.title,
            date: blog.createdAt,
            time_read: blog.readingTime,
            header_image: blog.header_image,
            description: blog.description,
            tags: blog.tags,
            path: blog.path,
          }"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Article from "~/components/Article";
import Header from "~/components/Header";
export default {
  components: { Article, Header },
  head() {
    return {
      title: "alvinscodes | blog",
    };
  },
  async asyncData({ $content, params }) {
    const blogs = await $content("blog").sortBy("createdAt").fetch();
    return { blogs };
  },
};
</script>

<style>
</style>