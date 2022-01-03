<template>
  <div>
    <Navbar />
    <Hero />
    <Services />
    <Articles />
    <Footer />
  </div>
  <router-view></router-view>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import Services from "./components/Services.vue";
import Articles from "./components/Articles.vue";
import Footer from "./components/Footer.vue";

export default defineComponent({
  name: "App",
  components: {
    Navbar,
    Hero,
    Services,
    Articles,
    Footer
},
  setup() {},
});
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Public+Sans:wght@100&display=swap");
#app {
  font-family: "Public Sans";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  margin: 0;
  padding: 0;
  background: #eee;
}
</style>
