<template>
  <section id="landing" class="relative">
    <div class="flex justify-center pt-24 md:pt-64 px-8">
      <div
        class="dark:text-gray-200 text-gray-900 text-center max-w-screen-md mx-auto relative z-30"
      >
        <div class="flex justify-center mb-8">
          <div class="relative">
            <img
              class="rounded-full border-2 animated-circle-outline w-32 relative z-20"
              alt="me"
              src="../assets/self-image.jpg"
            />
          </div>
        </div>
        <h1
          class="text-3xl md:text-5xl font-bold mb-4 dark:text-slate-200 text-slate-700"
        >
          Front-end Engineer <span class="text-emerald-400">&</span> UX Designer
        </h1>
        <p class="font-light mb-8 text-slate-600 dark:text-slate-400">
          Take a moment to explore my portfolio to see some of my past projects.
          Please feel free to reach out if you’d like to learn more.
        </p>
        <button
          class="text-slate-900 dark:text-white rounded-full py-2 bg-transparent px-6 transition duration-500 hover:shadow-lg hover:shadow-emerald-500/20 border border-emerald-400"
          @click="toggleWorkPage"
        >
          Explore my work
        </button>
      </div>
    </div>
    <div>
      <div class="py-24 md:py-64 px-8 md:px-4 max-w-screen-md mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-3 mb-4">
          <div class="md:col-span-2">
            <h3
              class="text-xl md:text-3xl font-bold mb-2 dark:text-slate-200 text-slate-700"
            >
              Demonstrated dedicated <span class="text-emerald-400">experience</span>
            </h3>
            <p class="font-light mb-5 text-slate-600 dark:text-slate-400">
              working with front-end builds and designs, including:
            </p>
          </div>
        </div>
        <div class="flex flex-wrap items-center gap-4 mb-4">
          <div
            class="cursor-pointer text-emerald-500 rounded-full py-1 text-sm inline-flex bg-transparent font-medium px-6 transition duration-500 hover:shadow-lg dark:hover:shadow-emerald-500/20 hover:shadow-emerald-500/20 border border-emerald-500"
            @click="toggleWorkPage"
          >
            # Admin Dashboards
          </div>
          <div
            class="cursor-pointer text-emerald-400 rounded-full py-1 text-sm inline-flex bg-transparent font-medium px-6 transition duration-500 hover:shadow-lg dark:hover:shadow-emerald-500/20 hover:shadow-emerald-500/20 border border-emerald-400"
            @click="toggleWorkPage"
          >
            # Branded Web Pages
          </div>
          <div
            class="cursor-pointer text-emerald-300 rounded-full py-1 text-sm inline-flex bg-transparent font-medium px-6 transition duration-500 hover:shadow-lg dark:hover:shadow-emerald-500/20 hover:shadow-emerald-500/20 border border-emerald-300"
            @click="toggleWorkPage"
          >
            # Logo Design
          </div>
          <div
            class="cursor-pointer text-emerald-200 rounded-full py-1 text-sm inline-flex bg-transparent font-medium px-6 transition duration-500 hover:shadow-lg dark:hover:shadow-emerald-500/20 hover:shadow-emerald-500/20 border border-emerald-200"
            @click="toggleWorkPage"
          >
            # Blog Graphics
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    toggleWorkPage() {
      this.$emit("toggle-work-page");
    },
  },
};
</script>

<style lang="scss" scoped></style>
