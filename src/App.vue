<template>
  <div id="app" class="flex">
    <Main
      description="As a Front-End developer since 10 years now, I enjoy creating beautiful apps on Javascript Frameworks."
      name="Guillaume Duhan."
      title="Creating web apps for start-ups."
    />
  </div>
</template>

<script>
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Main
  }
};
</script>

<style lang="css">
@import url("https://fonts.googleapis.com/css?family=Jost:300,400,500,600,700&display=swap");

#app {
  font-family: Jost;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
