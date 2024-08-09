<template>
  <div>
    <div class="digit-container">
      <div class="value">
        {{ formattedValue }}
      </div>
    </div>

    <div class="label">
      {{ label }}
    </div>
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
.digit-container {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  background-color: var(--dark-desaturated-blue);
  border-radius: 4px;
  width: 148px;
  height: 140px;
  /* width: 70px;
  height: 66.27px; */
}

.value {
  font-size: 80px;
  /* font-size: 36px; */
  color: var(--soft-red);
  text-align: center;
  letter-spacing: -2.4px;
  line-height: 71px;
}

.label {
  display: block;
  font-size: 14px;
  text-transform: uppercase;
  color: var(--grayish-blue);
  letter-spacing: 5.92px;
  text-align: center;
  margin-top: 10px;
}
</style>
