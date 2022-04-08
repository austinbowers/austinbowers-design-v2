<template>
  <Header/>
  <Landing/> 
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
