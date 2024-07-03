<script setup>
const props = defineProps({
    semillero: Object
});
</script>
<template>
    <div>
      <ul>
        <li v-for="semillero in semilleros" :key="semillero.nombre">
          {{ semillero.nombre }} - {{ semillero.facultad }}
        </li>
      </ul>
    </div>
  </template>
  <style scoped>
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    padding: 8px 0;
  }
  </style>

  