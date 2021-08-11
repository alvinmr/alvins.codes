<template></template>

<script>
export default {
  data() {
    return {
      url: "https://meet.google.com/ymy-jmcu-izg/",
    };
  },
  layout: "redirect",
  head() {
    return {
      meta: [
        {
          "http-equiv": "refresh",
          content: `0;url=${this.url}`,
        },
      ],
    };
  },
};
</script>

<style>
</style>