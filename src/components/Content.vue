<template>
    <div class="Content">
        <h2 class="text-xl-center"><strong>Un gestionnaire de tâches de confiance</strong></h2>

        <form class="mt-4">
            <div class="form-group">
                <label for="inputTodo" class="text-center">Saisir une tâche :</label>
                <input v-model="formData.todo" id="inputTodo" type="text" class="form-control">
            </div>
            <button v-on:click.prevent="addItem" class="btn btn-outline-primary">Créer une tâche</button>
        </form>

        <ul class="todo mt-5">
            <li v-bind:key="index" v-for="(todo, index) in tableTodo">
                <Item :id="index" :todo="todo" :deleteItem="deleteItem"/>
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
        methods: {
            addItem: function () {
                this.tableTodo.push(this.formData.todo);
                this.formData.todo = '';
            },
            deleteItem: function (e) {
                this.tableTodo.splice(e.target.parentNode.id, 1)
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
        padding: 0;
    }
</style>
