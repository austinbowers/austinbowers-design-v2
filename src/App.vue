<template class="relative">
  <Header />
  <LowerLeftNav />

  <section v-if="!workPage">
    <Landing @toggle-work-page="toggleWorkPage" />
    <FreelanceWebDesign />
  </section>
  <section v-if="workPage">
    <div
      class="dark:text-gray-200 text-gray-900 mx-auto max-w-screen-lg relative z-30"
    >
      <p @click="toggleWorkPage" class="cursor-pointer text-green-400">
        Back to home
      </p>
    </div>
    <div class="flex justify-center pt-24 pb-80 px-8">
      <div
        class="dark:text-gray-200 text-gray-900 text-center max-w-screen-lg relative z-30"
      >
        <div class="grid grid-cols-2 lg:grid-cols-3 gap-4">
          <div
            class="bg-white h-full w-full inline-flex items-center justify-center"
          >
            <img class="w-full" src="./assets/photos/Back.jpg" />
          </div>
          <div
            class="bg-white h-full w-full inline-flex items-center justify-center"
          >
            <img class="w-full" src="./assets/photos/Back2.jpg" />
          </div>
          <div
            class="bg-white h-full w-full inline-flex items-center justify-center"
          >
            <img class="w-full" src="./assets/photos/BHBWavy.png" />
          </div>
          <div
            class="bg-white h-full w-full inline-flex items-center justify-center"
          >
            <img class="w-full" src="./assets/photos/THE_ONE.png" />
          </div>
        </div>
      </div>
    </div>
  </section>
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
    FreelanceWebDesign,
  },
  data() {
    return {
      workPage: false,
    };
  },
  methods: {
    toggleWorkPage() {
      this.workPage = !this.workPage;
    },
  },
};
</script>

<style lang="scss">
body {
  @apply transition duration-300;
}
</style>
