<script setup>
import semillero from '../data/dataSemilleros.json'
</script>
<template>
  <div class="m-4">
    <Jrplaneacion :semillero="semillero[1]"/>
  </div>
</template>
