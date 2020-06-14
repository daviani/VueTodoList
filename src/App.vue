<template>
    <div id="app">
        <ComponentNavBar/>
        <img alt="Vue logo" src="./assets/logo.png">
        <ComponentContent/>
    </div>
</template>

<script>

    // Components
    import ComponentNavBar from "./components/NavBar";
    import ComponentContent from "./components/Content";

    export default {
        name: 'App',
        components: {
            ComponentNavBar,
            ComponentContent
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #35495e;
        margin-top: 10px;
    }
</style>
