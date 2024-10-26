<script setup lang="ts"></script>

<template>
  <a class="btn" href="#">Request Beta Access</a>
</template>

<style scoped>
:global(.btn) {
  display: inline-block;
  border-radius: 6px;
  transition: background-color 0.3s ease, color 0.3s ease;
  cursor: pointer;
}

.title-sm-bold {
  line-height: 32px;
}

.btn-header {
  border: 1px solid var(--clr-dark-blue);
  padding: 12px 24px;
  background-color: var(--clr-beige-light);
  color: var(--clr-dark-blue);
  letter-spacing: -0.18px;

  &:hover {
    background-color: var(--clr-dark-blue);
    color: var(--clr-beige-light);
  }
}

.btn-hero {
  padding: 14px 32px;
  background-color: var(--clr-dark-blue);
  color: var(--clr-beige-light);

  &:hover {
    background: var(--gradient-hover-btn);
  }
}
</style>
