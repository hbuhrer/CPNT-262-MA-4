<template>
  <div class="flex flex-col justify-center text-center h-screen text-5xl">
    <!-- Data binding: status variable is bound to text content -->
    <h1 class="font-bold font-sans">MICROSOFT HIRE ME</h1>
    <div class="flex flex-col justify-center text-center text-4xl sm:flex-row">
      <h2>BECAUSE &nbsp;</h2>
      <!-- Double mustache variable rendering (or squigly brackets): rendering the status variable -->
      <h2 class="text-green-600">{{ status }}</h2>
    </div>
  </div>
</template>

<script setup>
import { ref, watchEffect } from 'vue';

// Reactivity: using ref() to create reactive variables
const statuses = ref(["I NEED A JOB", "I'M SMART*", "I'M A HUMAN*", "I'M QUALIFIED-ISH", "I'M CREATIVE"]);
const currentIndex = ref(0);
const status = ref(statuses.value[currentIndex.value]);

watchEffect(() => {
  const interval = setInterval(() => {
    // Reactivity: updating reactive variable currentIndex.value
    currentIndex.value = (currentIndex.value + 1) % statuses.value.length;
    status.value = statuses.value[currentIndex.value]; // Reactivity: updating reactive variable status.value
  }, 3500);

  // Cleanup function
  return () => clearInterval(interval);
});
</script>