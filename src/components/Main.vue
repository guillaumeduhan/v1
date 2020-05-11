<template>
  <div
    class="Main relative min-h-screen min-w-full flex flex-col justify-center items-center bg-marine"
  >
    <header class="w-3/4 flex flex-col justify-center items-center mx-auto">
      <div data-aos="fade-down" v-if="imageUrl" class="flex items-center justify-center bg-marine overflow-hidden w-32 h-32 bg-cover bg-center rounded-full mb-8" :style="{ backgroundImage: `url('${imageUrl}')` }" />
      <h2 data-aos="fade-up" class="text-title font-semibold text-rouge leading-tight">{{ name }}</h2>
      <h1 data-aos="fade-up" class="text-title font-semibold text-light_white leading-none mb-12">{{ title }}</h1>
      <p data-aos="fade-up" class="w-3/6 text-light_white mb-12 opacity-75 text-base text-center">{{ description }}</p>
      <button data-aos="fade-up"
        class="bg-transparent text-center text-base hover:bg-rouge-500 text-rouge font-semibold hover:text-white py-2 px-4 border border-rouge hover:border-rouge rounded outline-none"
      >Contact</button>
    </header>
    <div
      data-aos="fade-up"
      class="social text-center bg-marine flex items-center text-2xl m-8"
    >
      <i
        v-for="(media, mediaIndex) in social"
        :key="mediaIndex"
        :class="'fab text-base text-light_white cursor-pointer m-2 opacity-25 hover:opacity-100 hover:text-rouge fa-' + mediaIndex"
        @click="openThis(media)"
      ></i>
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
  },
  methods: {
    openThis(url) {
      window.open(url, '_blank')
    }
  }
};
</script>
