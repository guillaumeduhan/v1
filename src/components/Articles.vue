<template>
  <div
    class="Articles relative min-h-screen min-w-full flex flex-col justify-start items-center bg-light_white"
  >
    <div class="w-3/4 mx-auto py-24">
      <h1
        data-aos="fade-right"
        class="font-semibold text-marine text-5xl leading-none mb-12"
      >{{ title }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: "Articles",
  props: {
    title: {
      default: "",
      type: String
    }
  }
};
</script>