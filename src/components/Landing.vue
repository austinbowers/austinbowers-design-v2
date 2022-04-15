<template>
  <section id="landing" class="dark:bg-gray-900 bg-white relative overflow-hidden">
    <div
      class="animated-blur-1 absolute w-64 h-64 rounded-full blur-2xl dark:bg-green-600 bg-green-400 top-0 z-10"
    ></div>
     <div
      class="animated-blur-2 absolute w-64 h-64 rounded-full blur-2xl dark:bg-blue-400 bg-blue-500 top-0 z-10"
    ></div>
    <div class="flex justify-center pt-40 pb-80 px-8">
      <div class="dark:text-gray-200 text-gray-900 text-center max-w-screen-md relative z-30">
        <div class="flex justify-center mb-8">
          <div class="relative">
            <img
              class="rounded-full border animated-circle-outline w-32 relative z-20"
              alt="me"
              src="../assets/self-image.jpg"
            />
          </div>
        </div>
        <h1 class="text-4xl md:text-6xl font-bold mb-5">
          Front-end Engineer & UX Designer
        </h1>
        <h6 class="font-light mb-8">
          Take a moment to explore my portfolio to see some of my past projects.
          Please feel free to reach out if you’d like to learn more.
        </h6>
        <button class="btn btn-green" @click="toggleWorkPage">View work</button>
      </div>
    </div>
  </section>
</template>

<script>
  export default {
    methods: {
      toggleWorkPage() {
        this.$emit('toggle-work-page');
      }
    }
  };
</script>

<style lang="scss" scoped>
    .animated-circle-outline {
      @apply border-green-400;
      animation: 5s linear infinite alternate ease-in-out; 
      animation-name: circle-outline-color-change;
    }
    .animated-blur-1 {
        animation: 30s linear infinite alternate ease-in-out; 
        animation-name: blur-move-1;
        opacity:0;
    }
    .animated-blur-2 {
        animation: 30s linear infinite alternate ease-in-out; 
        animation-name: blur-move-2;
        opacity:0;
    }

    @keyframes circle-outline-color-change {
        0% {
            @apply border-green-400;
        }
        50% {
            @apply border-blue-400; 
        }
        100% {
            @apply border-green-400;
        }
    }

    @keyframes blur-move-1 {
        0% {
            opacity:0;
            top: 20%;
            left: 20%;
        }
        50% {
            opacity:60;
            top: 60%;
            left: 80%;
        }
        100% {
            opacity:0;
            top: 20%;
            left: 0%;
        }
    }
    @keyframes blur-move-2 {
        0% {
            opacity:0;
            top: 10%;
            left: 50%;
        }
        50% {
             opacity:60;
            top: 40%;
            left: 10%;
        }
        100% {
            opacity: 0;
            top: 10%;
            left: 50%;
        }
    }
</style>
