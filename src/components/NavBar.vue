<template>
        <div class="header-top">
            <h1> <strong>A vue Todo List</strong></h1>
        </div>

</template>

<script>
    export default {
        name: 'navbar',
        props: {
        },
    };
</script>

<style scoped>
    .header-top {
        position: fixed;
        top: 0;
        height: 50px;
        width: 100%;
        background: #41b883;
        color: #35495e;
        text-align: center;
        line-height: 50px;
        font-size: 25px;
    }
</style>
