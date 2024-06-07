<script setup>

const props = defineProps({
    nombreSemillero: String,
    integrantes: Array,
    mision: String,
    vision: String,
    resumen: String,
})
</script>
<template>
    <div>
        <Card>
            <template #title>{{ props.nombreSemillero }}</template>
            <template #content>
                <Accordion :activeIndex="0">
                    <AccordionTab header="Misión">
                        <p class="m-0">
                            {{ props.mision }}
                        </p>
                    </AccordionTab>
                    <AccordionTab header="Visión">
                        <p class="m-0">
                            {{ props.vision }}
                        </p>
                    </AccordionTab>
                </Accordion>

                <DataTable :value="props.integrantes">
                    <template #header>
                        <div class="flex flex-wrap justify-content-end gap-2">
                            Integrantes
                        </div>
                    </template>
                    <Column field="nombre" header="Nombre"></Column>
                    <Column field="identificacion" header="Nit"></Column>
                    <Column field="nivelAcademico" header="Nivel Academico"></Column>
                </DataTable>
            </template>
        </Card>
    </div>
</template>