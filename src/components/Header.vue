<template>
    <div class="flex justify-between dark:bg-gray-900 bg-white w-full z-50 items-center h-16 px-8">
        <div></div>
        <ThemeToggler/>
    </div>
</template>

<script>
import ThemeToggler from '../components/ThemeToggler.vue'

export default {
    components: {
        ThemeToggler
    }
}
</script>

<style>

</style>