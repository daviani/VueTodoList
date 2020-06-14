<template>
    <div class="card m-4 p-4 todo">
        <p> {{todo}} </p>
        <div class="btn-delete btn btn-outline-danger"><strong>X</strong></div>
    </div>
</template>

<script>
    export default {
        name: 'Item',
        props: ['todo', 'delete'],
    };
</script>
<style scoped>
    .todo {
        text-align: left;
        position: relative;
        padding: 20px 160px 20px 30px;
        font-size: 20px;
        height: 80px;
    }

    .btn-delete {
        position: absolute;
        top: 20px;
        right: 20px;
        border-radius: 20px;
        color: #41b883;
        border-color: #41b883;
    }

    .btn-delete:hover {
        color: #ffffff;
        background-color: #41b883;
        border-color: #41b883;
    }

    .btn-delete:active {
        background-color: #41b883;
    }

</style>
