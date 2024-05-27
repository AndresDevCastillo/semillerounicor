<template>
    <div class="card">
        <div class="card-header">
        <slot name="header"></slot>
        </div>
        <div class="card-body">
        <slot name="body"></slot>
        </div>
    </div>
</template>

<script>
    export default {
    name: 'Card'
};
</script>

<style scoped>
    .card {
    border: 1px solid #000;
    border-radius: 8px;
    background-color: cyan;
    color: black;
    max-width: 400px;
    margin: 20px auto;
    padding: 20px;
}

    .card-header {
    font-weight: bold;
    font-size: 1.5em;
    margin-bottom: 10px;
}

    .card-body {
    font-size: 1em;
}
</style>  