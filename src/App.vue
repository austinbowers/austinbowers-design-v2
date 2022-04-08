<template class="relative">
  <Header />
  <LowerLeftNav/>

  <Landing />
  <FreelanceWebDesign/>
  
</template>

<script>
import Header from "./components/Header.vue";
import Landing from "./components/Landing.vue";
import LowerLeftNav from "./components/LowerLeftNav.vue";
import FreelanceWebDesign from "./components/FreelanceWebDesign.vue";

export default {
  components: {
    Header,
    Landing,
    LowerLeftNav,
    FreelanceWebDesign
  },
};
</script>

<style lang="scss">
body {
  @apply transition duration-300;
}
</style>
