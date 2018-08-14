<template>
    <div>
        <h1>To-Do List with Vue</h1>
        <input v-model.trim="task">
        <button @click="addTask" type="button">Adicionar</button>
        <ul>
            <li v-for="task in tasks" :key="task">{{ task }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "ToDoList",
    data() {
        return {
            task: "",
            tasks: [ "Task 1", "Task 2", "Task 3", "Task 4" ]
        }
    },
    methods: {
        addTask() {
            this.tasks.push(this.task)
            this.task = ""
        }
    }
}
</script>

