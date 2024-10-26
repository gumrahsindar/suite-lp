<script setup lang="ts">
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Testimonial from './components/Testimonial.vue'
import BaseLayout from './layouts/BaseLayout.vue'
</script>

<template>
  <BaseLayout>
    <template #header>
      <Header />
    </template>
    <template #main>
      <Hero />
      <Testimonial />
    </template>
    <template #footer>
      <Footer />
    </template>
  </BaseLayout>
</template>

<style scoped></style>
