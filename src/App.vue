<template>
  <header>
    We’re launching soon
  </header>

  <main>
    <!-- timer here -->
    <Digit label="days" value="0" />

  </main>

  <footer>
    <!-- social media here -->
  </footer>
</template>

<script setup>
import Digit from '@/components/Digit.vue';

</script>

<style scoped>

header {
  text-transform: uppercase;
  color: var(--white);
  font-size: 22px;
  letter-spacing: 7.5px;
  text-align: center;
}

main {
  background-image: url('@/assets/images/bg-stars.svg');
  display: flex;
  flex-direction: column;
  height: 70vh;
}

</style>
