<script setup>

const props = defineProps({
  semillero: Object
})

</script>

<template>
    <div class="planeacion">
        <div class="card">
            <Card>
                <template #content>
                    <TabView>
                        <TabPanel header="Estrategias">
                            <Accordion>
                                <AccordionTab header="Misión">
                                    <p class="m-0">{{ semillero.mision }}</p>
                                </AccordionTab>
                                <AccordionTab header="Visión">
                                    <p class="m-0">{{ semillero.vision }}</p>
                                </AccordionTab>
                                <AccordionTab header="Objetivos">
                                    <Accordion>
                                        <AccordionTab header="Objetivo General">
                                            <p class="m-0">{{ semillero.objetivoGeneral }}</p>
                                        </AccordionTab>
                                        <AccordionTab header="Objetivos Específicos">
                                            <ul>
                                                <li v-for="objetivo in semillero.objetivosEspecificos" :key="objetivo">
                                                    {{ objetivo }}
                                                </li>
                                            </ul>
                                        </AccordionTab>
                                    </Accordion>
                                </AccordionTab>
                                <AccordionTab header="Actividades">
                                    <ul>
                                        <li v-for="actividad in semillero.actividades" :key="actividad">
                                            {{ actividad }}
                                        </li>
                                    </ul>
                                </AccordionTab>
                                <AccordionTab header="Proyectos">
                                    <ul>
                                        <li v-for="proyecto in semillero.proyectos" :key="proyecto.nombre">
                                            <strong>{{ proyecto.nombre }}</strong> - {{ proyecto.tipo }} ({{ proyecto.estado }}) en {{ proyecto.campoSaber }}
                                        </li>
                                    </ul>
                                </AccordionTab>
                                <AccordionTab header="Publicaciones">
                                    <ul>
                                        <li v-for="publicacion in semillero.publicaciones" :key="publicacion.titulo">
                                            <strong>{{ publicacion.titulo }}</strong> ({{ publicacion.anio }}) - {{ publicacion.medio }}
                                        </li>
                                    </ul>
                                </AccordionTab>
                            </Accordion>
                        </TabPanel>
                    </TabView>
                </template>
            </Card>
        </div>
    </div>
</template>