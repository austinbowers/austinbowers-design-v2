<template class="relative">
  <Header/>
  <Landing/> 
  <div class="fixed left-5 bottom-5">
      <div class="absolute left-1 bottom-1 h-24 w-1 border-l border-gray-700 dark:border-gray-500"></div>
      <div class="absolute left-1 bottom-1 w-24 md:w-48 h-1 border-b border-gray-700 dark:border-gray-500"></div>
      <div class="relative z-50 flex items-center mb-5 ml-6 dark:text-white text-gray-700 font-light">
        <a class=" cursor-pointer mr-5 p-3 hover:text-green-400">
            Home
        </a>
        <a class=" cursor-pointer mr-5 p-3 hover:text-green-400">
            Work
        </a>
        <a class=" cursor-pointer mr-5 p-3 hover:text-green-400">
            Contact
        </a>
      </div>
  </div>
</template>

<script>
    import Header from './components/Header.vue'
    import Landing from './components/Landing.vue'

    export default {
        components: {
            Header, 
            Landing
        }
    }
</script> 

<style lang="scss">
    body {
      @apply transition duration-300;
    }
</style>
