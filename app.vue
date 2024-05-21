<template>
  <component :is="comp" />
  <button @click="toggle = !toggle">Show</button>
</template>
<script setup>
const toggle = ref(false);

const comp = computed(() => toggle.value ? getTestComponent('Test') : null);
</script>
