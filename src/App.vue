<template>
  <header>
    We’re launching soon
  </header>

  <main class="countdown">
    <!-- timer here -->
    <Digit label="days" value="8" />
    <Digit label="hours" value="23" />
    <Digit label="minutes" value="55" />
    <Digit label="seconds" value="41" />

  </main>

  <footer>
    <!-- social media here -->
  </footer>
</template>

<script setup>
import Digit from '@/components/Digit.vue';

</script>

<style scoped>
.countdown {
  display: flex;
  flex-direction: row;
  gap: 32px;
  justify-content: center;
  align-items: center;
}

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
