<template>
  <div class="container">
    <div class="custom-card">
      <div class="header">
        <Avatar class="avatar" image="https://primefaces.org/cdn/primereact/images/avatar/amyelsner.png" shape="circle" />
        <div class="card-content">
          <Card style="background: none; box-shadow: none;">
            <template v-slot:title>{{ semillero.nombre }}</template>
            <template v-slot:content>
              {{ semillero.objetivoGeneral }}
            </template>
          </Card>
        </div>
      </div>
      <Divider layout="horizontal" type="dashed" class="p-mb-3"/>
      <TabView>
        <TabPanel header="Mision">
          {{ semillero.mision }}
        </TabPanel>
        <TabPanel header="Vision">
          {{ semillero.vision }}
        </TabPanel>
        <TabPanel header="Objetivos Especificos">
          <ul>
            <li v-for="objetivo in semillero.objetivosEspecificos" :key="objetivo">
              {{ objetivo }}
            </li>
          </ul>
        </TabPanel>
      </TabView>
    </div>
  </div>
</template>

<script setup>

const props = defineProps({
    semillero: Object
})

</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
}

.custom-card {
  width: 800px;
  border-radius: 15px;
  background: linear-gradient(90deg, #141e30, #243b55);
  padding: 20px;
}

.header {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.avatar {
  width: 200px;
  height: 100px;
  margin-right: 20px;
}

.card-content {
  flex-grow: 1;
}

.p-card {
  color: #ffffff;
}

.p-card .p-card-header {
  color: #ffffff;
}
</style>
