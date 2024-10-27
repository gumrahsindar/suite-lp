<script setup lang="ts"></script>

<template>
  <header>
    <slot name="header"></slot>
  </header>
  <main>
    <slot name="main"></slot>
  </main>
  <footer id="footer">
    <slot name="footer"></slot>
  </footer>
</template>

<style>
#footer {
  position: relative;
}
</style>
