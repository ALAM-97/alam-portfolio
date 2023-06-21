<template>
  <SectionOne />
  <SectionTwo />
  <SectionThree />
  <SectionFour />
</template>

<script>
import SectionOne from "./homepage/SectionOne.vue";
import SectionTwo from "./homepage/SectionTwo";
import SectionThree from "./homepage/SectionThree";
import SectionFour from "./homepage/SectionFour";

export default {
  name: "AlamHome",
  components: { SectionOne, SectionTwo, SectionThree, SectionFour },
};
</script>

<style lang="scss">
.page {
  height: 100vh;
  scroll-snap-align: start;
  scroll-snap-stop: always;
  padding-left: 6.25rem;
  padding-right: 6.25rem;
  color: #262626;
  .page-content {
    height: 100%;
    display: flex;
    max-width: 120rem;
    margin: 0 auto;
  }
}
/* text */
h1,
h2 {
  font-size: 5.625rem;
  font-family: Kollektif;
}
p {
  font-family: Montserrat;
  font-weight: 400;
  font-size: 1.75rem;
  line-height: 2.5rem;
  margin-top: 1.25rem;
}
</style>
