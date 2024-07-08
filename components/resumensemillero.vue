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
            <template #header>
                <div class="flex justify-center items-center mt-3">
                    <Avatar image="https://universidadesgratuitas.com/wp-content/uploads/2020/09/escudo-universidad-de-cordoba-1159x1536.png" class="mr-2" size="xlarge" shape="circle" />
                    <h1>{{props.nombreSemillero}}</h1>
                </div>
            </template>
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

                <DataTable :value="props.integrantes" showGridlines stripedRows>
                    <template #header>
                        <div class="flex flex-wrap justify-content-end gap-2">
                            Integrantes
                        </div>
                    </template>
                    <Column field="nombre" header="Nombre"></Column>
                    <Column field="identificacion" header="Nit"></Column>
                    <Column header="Nivel Academico">
                        <template #body= {data}>
                            <Badge :value="data.nivelAcademico"></Badge>
                        </template>
                    </Column>
                </DataTable>
            </template>
        </Card>
    </div>
</template>