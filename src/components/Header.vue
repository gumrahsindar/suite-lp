<script setup lang="ts">
import Button from './Button.vue'
import Logo from './Logo.vue'
</script>

<template>
  <div class="container">
    <div class="layout">
      <Logo />
      <Button class="btn-header title-sm-bold" />
    </div>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 50px;

  @media (max-width: 64rem) {
    padding-top: 40px;
  }

  @media (max-width: 48rem) {
    padding-top: 24px;
  }
}
</style>
