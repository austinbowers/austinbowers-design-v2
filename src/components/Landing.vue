<template>
  <section id="landing" class="dark:bg-gray-900 bg-white relative">
    <div class="flex justify-center pt-24 md:pt-40 pb-72 px-8">
      <div class="dark:text-gray-200 text-gray-900 text-center max-w-screen-md relative z-30">
        <div class="flex justify-center mb-8">
          <div class="relative">
            <img
              class="rounded-full border-2 animated-circle-outline w-32 relative z-20"
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
  }
</script>

<style lang="scss" scoped>

</style>