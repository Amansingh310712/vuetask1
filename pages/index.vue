<template>
  <div>
    <Navbar/>
    <Scale/>
    <Highlightingpart/>
    <!-- <Review/> -->
    <Helping/>
    <Footer/>
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue';
import Highlightingpart from '~/components/Highlightingpart.vue';
import Footer from '~/components/Footer.vue'
import Scale from '~/components/Scale.vue'
import Helping from '~/components/Helping.vue'
// import Review from '~/components/Review.vue'
useHead({
  title: "Pinwheel-tailwind"
})
</script>

<style>


</style>
  