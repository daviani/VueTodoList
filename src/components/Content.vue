<template>
    <div class="Content">
        <h2 class="text-xl-center"><strong>Un gestionnaire de tâches de confiance</strong></h2>

        <form class="mt-4">
            <div class="form-group">
                <label for="inputTodo" class="text-center">Saisir une tâche :</label>
                <input id="inputTodo" type="text" class="form-control">
            </div>
            <div class="btn btn-outline-primary">Créer une tâche</div>
        </form>

        <ul class="todo mt-5">
            <li v-bind:key="index" v-for="(todo, index) in tableTodo">
                <Item v-bind:todo="todo"/>
            </li>
        </ul>
    </div>
</template>
<script>

    import Item from "./Item";

    export default {
        name: 'Content',
        data() {
            return {
                formData: {
                    todo: ''
                },
                tableTodo: ['5', '4', '3', '2', '1'],
            }
        },
        components: {
            Item
        }

    };
</script>

<style>
    li {
        list-style: none;
    }
</style>
