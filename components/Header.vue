<template>
  <div class="flex w-full mt-24 h-80">
    <div
      class="relative self-center p-5 mx-auto bg-white border-2 border-black lg:p-12 intro lg:w-10/12 shadow-theme rounded-theme"
    >
      <svg
        width="300"
        height="230"
        viewBox="0 0 463 220"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        class="absolute dots"
      >
        <circle cx="10" cy="10" r="10" fill="black" />
        <circle cx="50" cy="10" r="10" fill="black" />
        <circle cx="90" cy="10" r="10" fill="black" />
        <circle cx="130" cy="10" r="10" fill="black" />
        <circle cx="170" cy="10" r="10" fill="black" />
        <circle cx="210" cy="10" r="10" fill="black" />
        <circle cx="10" cy="50" r="10" fill="black" />
        <circle cx="50" cy="50" r="10" fill="black" />
        <circle cx="90" cy="50" r="10" fill="black" />
        <circle cx="130" cy="50" r="10" fill="black" />
        <circle cx="170" cy="50" r="10" fill="black" />
        <circle cx="210" cy="50" r="10" fill="black" />
        <circle cx="10" cy="90" r="10" fill="black" />
        <circle cx="50" cy="90" r="10" fill="black" />
        <circle cx="90" cy="90" r="10" fill="black" />
        <circle cx="130" cy="90" r="10" fill="black" />
        <circle cx="170" cy="90" r="10" fill="black" />
        <circle cx="210" cy="90" r="10" fill="black" />
        <circle cx="10" cy="130" r="10" fill="black" />
        <circle cx="50" cy="130" r="10" fill="black" />
        <circle cx="90" cy="130" r="10" fill="black" />
        <circle cx="130" cy="130" r="10" fill="black" />
        <circle cx="170" cy="130" r="10" fill="black" />
        <circle cx="210" cy="130" r="10" fill="black" />
        <circle cx="10" cy="170" r="10" fill="black" />
        <circle cx="50" cy="170" r="10" fill="black" />
        <circle cx="90" cy="170" r="10" fill="black" />
        <circle cx="130" cy="170" r="10" fill="black" />
        <circle cx="170" cy="170" r="10" fill="black" />
        <circle cx="210" cy="170" r="10" fill="black" />
        <circle cx="10" cy="210" r="10" fill="black" />
        <circle cx="50" cy="210" r="10" fill="black" />
        <circle cx="90" cy="210" r="10" fill="black" />
        <circle cx="130" cy="210" r="10" fill="black" />
        <circle cx="170" cy="210" r="10" fill="black" />
        <circle cx="210" cy="210" r="10" fill="black" />
        <circle cx="253" cy="10" r="10" fill="black" />
        <circle cx="293" cy="10" r="10" fill="black" />
        <circle cx="333" cy="10" r="10" fill="black" />
        <circle cx="373" cy="10" r="10" fill="black" />
        <circle cx="413" cy="10" r="10" fill="black" />
        <circle cx="453" cy="10" r="10" fill="black" />
        <circle cx="253" cy="50" r="10" fill="black" />
        <circle cx="293" cy="50" r="10" fill="black" />
        <circle cx="333" cy="50" r="10" fill="black" />
        <circle cx="373" cy="50" r="10" fill="black" />
        <circle cx="413" cy="50" r="10" fill="black" />
        <circle cx="453" cy="50" r="10" fill="black" />
        <circle cx="253" cy="90" r="10" fill="black" />
        <circle cx="293" cy="90" r="10" fill="black" />
        <circle cx="333" cy="90" r="10" fill="black" />
        <circle cx="373" cy="90" r="10" fill="black" />
        <circle cx="413" cy="90" r="10" fill="black" />
        <circle cx="453" cy="90" r="10" fill="black" />
        <circle cx="253" cy="130" r="10" fill="black" />
        <circle cx="293" cy="130" r="10" fill="black" />
        <circle cx="333" cy="130" r="10" fill="black" />
        <circle cx="373" cy="130" r="10" fill="black" />
        <circle cx="413" cy="130" r="10" fill="black" />
        <circle cx="453" cy="130" r="10" fill="black" />
        <circle cx="253" cy="170" r="10" fill="black" />
        <circle cx="293" cy="170" r="10" fill="black" />
        <circle cx="333" cy="170" r="10" fill="black" />
        <circle cx="373" cy="170" r="10" fill="black" />
        <circle cx="413" cy="170" r="10" fill="black" />
        <circle cx="453" cy="170" r="10" fill="black" />
        <circle cx="253" cy="210" r="10" fill="black" />
        <circle cx="293" cy="210" r="10" fill="black" />
        <circle cx="333" cy="210" r="10" fill="black" />
        <circle cx="373" cy="210" r="10" fill="black" />
        <circle cx="413" cy="210" r="10" fill="black" />
        <circle cx="453" cy="210" r="10" fill="black" />
      </svg>
      <h1 class="text-3xl lg:text-5xl font-brandonBlack">{{ title }}</h1>
      <p v-if="hasDescription" class="text-base lg:text-2xl">{{ desc }}</p>
      <div class="flex items-center justify-between mt-32" v-else>
        <div class="flex flex-row">
          <svg
            width="30"
            height="30"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M3 6C3 4.89543 3.89543 4 5 4H19C20.1046 4 21 4.89543 21 6V20C21 21.1046 20.1046 22 19 22H5C3.89543 22 3 21.1046 3 20V6Z"
              stroke="#000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
            <path
              d="M3 10H21"
              stroke="#000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
            <path
              d="M16 2V6"
              stroke="#000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
            <path
              d="M8 2V6"
              stroke="#000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
          </svg>
          <p
            class="self-center ml-3 text-xs font-bold text-gray-800 lg:text-xl"
          >
            {{ `${date}` }}
          </p>
        </div>
        <div class="flex flex-row">
          <svg
            width="32"
            height="32"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
            class="-mr-2"
          >
            <circle
              cx="12"
              cy="12"
              r="10"
              stroke="#000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></circle>
            <path
              d="M12 6V12L16 16"
              stroke="#000"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            ></path>
          </svg>
          <p
            class="self-center w-8/12 ml-0 text-xs font-semibold text-right text-gray-800 lg:w-full lg:ml-3 lg:text-xl"
          >
            {{ `${time_read} minute read` }}
          </p>
        </div>
      </div>
      <svg
        height="200"
        viewBox="0 0 236 220"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        class="absolute circle"
      >
        <circle cx="126" cy="110" r="110" fill="#75B6E4" />
        <circle cx="110" cy="110" r="109.5" stroke="black" />
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    hasDescription: Boolean,
    desc: String,
    title: String,
    author: String,
    date: String,
    time_read: Number,
  },
};
</script>

<style>
.dots {
  left: -10rem;
  top: -2rem;
  z-index: -1;
  height: 100px;
}

.circle {
  bottom: -4rem;
  right: -1rem;
  z-index: -2;
  height: 100px;
}

@screen lg {
  .dots {
    left: -6rem;
    top: -9rem;
    height: 100%;
  }

  .circle {
    right: -8rem;
    bottom: -6rem;
    height: 100%;
  }
}
</style>