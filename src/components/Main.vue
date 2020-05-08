<template>
  <div
    class="Main relative min-h-screen min-w-full flex flex-col justify-center items-center bg-marine"
  >
    <header data-aos="fade-up" class="w-3/4 mx-auto">
      <h2 class="font-semibold text-rouge text-7xl leading-tight">{{ name }}</h2>
      <h1 class="font-semibold text-light_white text-7xl leading-none mb-12">{{ title }}</h1>
      <p class="w-2/6 text-light_white mb-12 opacity-75 text-lg">{{ description }}</p>
      <button
        class="bg-transparent hover:bg-rouge-500 text-rouge font-semibold hover:text-white py-2 px-4 border border-rouge hover:border-rouge rounded outline-none text-lg"
      >Contact me</button>
    </header>
    <div
      data-aos="fade-right"
      class="social flex flex-col items-center text-2xl absolute left-0 ml-4 bottom-0"
    >
      <i
        v-for="(media, mediaIndex) in social"
        :key="mediaIndex"
        :class="'fab text-light_white cursor-pointer m-2 opacity-25 hover:opacity-100 hover:text-rouge fa-' + mediaIndex"
      ></i>
      <div class="h-32 w-1 bg-light_white opacity-25"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Main",
  props: {
    description: {
      type: String,
      default: ""
    },
    imageUrl: {
      type: String,
      default: ""
    },
    name: {
      type: String,
      default: ""
    },
    social: {
      type: Object,
      default: () => {}
    },
    title: {
      type: String,
      default: ""
    }
  }
};
</script>
