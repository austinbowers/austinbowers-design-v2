<template class="relative">
  <div class="relative overflow-hidden min-h-screen">
    <Header />
    <section class="z-30" v-if="!workPage">
      <Landing @toggle-work-page="toggleWorkPage" />
      <!-- <FreelanceWebDesign /> -->
    </section>
    <section class="z-30" v-if="workPage">
      <div
        class="px-8 dark:text-gray-200 text-gray-900 mx-auto max-w-screen-lg relative mt-24 z-30"
      >
        <p @click="toggleWorkPage" class="cursor-pointer text-green-400 mb-8">
          Back to home
        </p>
        <div
          class="dark:text-gray-200 text-gray-900 text-center max-w-screen-lg relative z-30"
        >
          <div class="grid grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6 lg:gap-10">
            <div
              class="bg-white rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/Back.jpg" />
            </div>
            <div
              class="bg-white rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/Back2.jpg" />
            </div>
            <div
              class="bg-white rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/BHBWavy.png" />
            </div>
            <div
              class="bg-white rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/THE_ONE.png" /> 
            </div>
            <!-- <div
              class="bg-white col-span-2 rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/Roofing-calc.png" />
            </div>
            <div
              class="bg-white col-span-2 lg:col-span-3 rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/SolarReviewsHP.png" />
            </div>
            <div
              class="bg-white col-span-2 lg:col-span-3 rounded-md overflow-hidden h-full w-full inline-flex items-center justify-center"
            >
              <img class="w-full" src="./assets/photos/management-screen.png" />
            </div> -->
          </div>
        </div>
      </div>
    </section>
    <div
      class="animated-blur-1 absolute rounded-full blur-2xl dark:bg-emerald-500 bg-emerald-300 top-0 z-20"
    ></div>
    <div
      class="animated-blur-2 absolute rounded-full blur-2xl dark:bg-blue-500 bg-blue-300 top-0 z-10"
    ></div>
  </div>
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
.animated-circle-outline {
  @apply border-emerald-400;
  animation: 6s linear infinite alternate ease-in-out;
  animation-name: circle-outline-color-change;
}
.animated-blur-1 {
  animation: 35s linear infinite alternate ease-in-out;
  animation-name: blur-move-1;
  opacity: 0;
}
.animated-blur-2 {
  animation: 35s linear infinite alternate ease-in-out;
  animation-name: blur-move-2;
  opacity: 0;
}

@keyframes circle-outline-color-change {
  0% {
    @apply border-emerald-400;
  }
  50% {
    @apply border-blue-400;
  }
  100% {
    @apply border-emerald-400;
  }
}

@keyframes blur-move-1 {
  0% {
    opacity: 0;
    top: 5%;
    left: 5%;
    right: 40%;
    height: 20rem;
    width: 20rem;
  }
  50% {
    opacity: 70%;
    top: 60%;
    left: 80%;
    right: 20%;
    height: 25rem;
    width: 25rem;
  }
  100% {
    opacity: 0;
    top: 5%;
    left: 5%;
    right: 40%;
    height: 20rem;
    width: 20rem;
  }
}
@keyframes blur-move-2 {
  0% {
    opacity: 0;
    top: 10%;
    left: 50%;
    right: 0%;
    height: 20rem;
    width: 20rem;
  }
  50% {
    opacity: 70%;
    top: 0%;
    right: 100%;
    left: 0%;
    height: 30rem;
    width: 30rem;
  }
  100% {
    opacity: 0;
    top: 10%;
    left: 50%;
    right: 0%;
    height: 20rem;
    width: 20rem;
  }
}
</style>
