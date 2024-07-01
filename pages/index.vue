<template>
  <div class="m-4">
    <ExampleComponent :semillero="semillero[0]"/>
  </div>
</template>

<script setup>
import semillero from '../data/Semillero.json'
</script>