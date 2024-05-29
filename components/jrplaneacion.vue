<script setup>
import semillero from '../data/Semillero.json'

</script>
<template>
    <div class="planeacion">
        <div class="card">
            <Card>
                <template #content>
                    <TabView>
                        <TabPanel header="Estrategias">
                            <Accordion>
                                <AccordionTab v-for="estrategia in semillero[0].estrategias" :header="estrategia">
                                    <p class="m-0">
                                        Sin ningun texto
                                    </p>
                                </AccordionTab>
                               
                            </Accordion>
                        </TabPanel>


                    </TabView>
                </template>
            </Card>
        </div>
    </div>
</template>