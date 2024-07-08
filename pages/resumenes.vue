<script setup>
import semilleros from '../data/semillero.json'

const semillero = semilleros[0]

</script>
<template>
  <div class="flex justify-center">
    <Resumensemillero class="w-1/2 m-4" :nombreSemillero="semillero.nombre" :vision="semillero.vision" :mision="semillero.mision" :integrantes="semillero.integrantes.estudiantes"/>
  </div>
</template>
