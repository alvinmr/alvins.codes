<template>
  <div>
    <div class="article">
      <!-- <div class="image-article" :style="`background-image: url('${article.header_image}')`"></div> -->
      <div>
        <div class="relative flex flex-row justify-between">
          <p class="text-sm date lg:text-base">
            {{ $moment(article.date).format("Do MMM YYYY") }}
          </p>
          <p class="time">{{ timeRead(article.time_read) }} min read</p>
        </div>
        <nuxt-link
          :to="`${article.path}`"
          class="title-article hover:text-gray-700"
          exact
          >{{ article.title }}</nuxt-link
        >
        <p class="h-20 mt-4 mb-2 text-sm lg:mb-12 lg:text-base">
          {{ article.description }}
        </p>
        <div class="relative flex flex-row justify-between">
          <div class="flex flex-row bg-whiteTheme">
            <div v-for="tags in article.tags" :key="tags.index">
              <nuxt-link
                class="text-xs lg:text-base tags hover:text-gray-700"
                to="/"
                exact
              >
                #
                <span class="-ml-2 font-bold">{{ tags }}</span>
              </nuxt-link>
            </div>
          </div>
          <div class="pl-5 bg-whiteTheme">
            <nuxt-link
              class="text-xs lg:text-sm btn-article"
              :to="`${article.path}`"
              exact
              >Read Post</nuxt-link
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["article"],
  methods: {
    timeRead(milisecond) {
      return Math.floor(milisecond / 60000);
    },
  },
};
</script>

<style>
.image-article {
  @apply w-full h-64 bg-gray-600 rounded-lg;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.article {
  @apply flex flex-col justify-center mb-20;
  max-height: 1000px;
}

.title-article {
  @apply mt-8 text-4xl transition-colors font-brandonBlack;
  transition: 0.5s ease;
}

.time {
  @apply pl-5 mt-4 font-normal text-sm;
  background-color: #f6f6f6;
}

.date {
  @apply pr-5 mt-4 font-medium;
  background-color: #f6f6f6;
}

.date::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  right: 0;
  margin-top: 0.6rem;
  background-color: rgba(97, 97, 97, 0.335);
  z-index: -1;
}

.tags {
  @apply p-2 bg-orange-300 mr-2 rounded-lg;
}

.btn-article {
  @apply px-4 py-2 border border-black rounded-md bg-white;
  transition: 0.2s ease-in;
  box-shadow: 4px 4px 0px #1b262c;
}

.btn-article::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  left: 0;
  margin-top: 0.8rem;
  background-color: rgba(97, 97, 97, 0.335);
  z-index: -1;
}

@screen lg {
  .btn-article:hover {
    box-shadow: 0px 0px 0px #1b262c;
  }
}
</style>