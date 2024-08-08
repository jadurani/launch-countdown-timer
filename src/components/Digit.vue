<template>
  <div class="value">
    {{ formattedValue }}
  </div>

  <div class="label">
    {{ label }}
  </div>
</template>

<script setup>
import { computed, defineProps } from "vue";

const { label, value } = defineProps({
  label: String,
  value: String,
});

const formattedValue = computed(() => value.padStart(2, "0"));
</script>

<style scoped>
.value {
  font-size: 80px;
  color: var(--soft-red);
  text-align: center;
  letter-spacing: -2.4px;
  line-height: 71px;
}

.label {
  font-size: 14px;
  text-transform: uppercase;
  color: var(--grayish-blue);
  letter-spacing: 5.92px;
  text-align: center;
  margin-top: 10px;
}
</style>
