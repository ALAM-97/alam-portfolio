<template>
  <div class="container">
    <Header />
    <Home />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Home from "./components/Home.vue";

export default {
  name: "App",
  components: {
    Header,
    Home,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600&display=swap");
@font-face {
  font-family: Kollektif;
  src: url("./assets/font/Kollektif.ttf");
}
#app {
  font-family: Kollektif, Helvetica, Arial, sans-serif;
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  scroll-behavior: smooth;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
  &::-webkit-scrollbar {
    display: none;
  }
}
.container {
  scroll-snap-type: y mandatory;
  overflow-y: scroll;
  height: 100vh;
}
a {
  text-decoration: none;
  color: inherit;
}
</style>
