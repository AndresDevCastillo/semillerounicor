<template>
    <div class="container">
        <div class="avatar">
        <Avatar image="https://www.primefaces.org/wp-content/uploads/2020/05/placeholder.png" shape="circle" size="large" />
        </div>
        <div class="card">
        <Card title="Título de la Tarjeta">
            <p>Contenido de la tarjeta</p>
        </Card>
        </div>
        <div class="tab-menu">
        <TabMenu :model="items" />
        </div>
    </div>
</template>

<script>
    import Avatar from 'primevue/avatar';
    import Card from 'primevue/card';
    import TabMenu from 'primevue/tabmenu';

    export default {
    components: {
        Avatar,
        Card,
        TabMenu
    },
    data() {
        return {
        items: [
            {label: 'Tab 1', icon: 'pi pi-fw pi-home'},
            {label: 'Tab 2', icon: 'pi pi-fw pi-calendar'},
            {label: 'Tab 3', icon: 'pi pi-fw pi-pencil'}
        ]
        };
    }
    };
</script>

<style scoped>
    .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 300px; /* ajusta el tamaño según sea necesario */
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

    .avatar {
    margin-bottom: 20px;
}

    .card {
    width: 100%;
    margin-bottom: 20px;
}

    .tab-menu {
    width: 100%;
    }
</style>