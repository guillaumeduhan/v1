<template>
  <div id="app" class="flex flex-col">
    <Main
      :social="links"
      description="As a Front-End developer since 10 years now, I enjoy creating beautiful apps on Javascript Frameworks."
      :imageUrl="portrait"
      name="Guillaume Duhan."
      title="Creating web apps."
    />
  </div>
</template>

<script>
import Main from "./components/Main.vue";
import portrait from "../src/assets/portrait.jpg"

export default {
  name: "App",
  components: {
    Main
  },
  data() {
    return {
      portrait,
      links: {
        facebook: "https://www.facebook.com/groups/javascript.paris",
        twitter: "https://www.facebook.com/groups/javascript.paris",
        instagram: "https://www.facebook.com/groups/javascript.paris",
        youtube: "https://www.facebook.com/groups/javascript.paris",
        github: "https://www.facebook.com/groups/javascript.paris"
      }
    };
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
