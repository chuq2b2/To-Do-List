<template>
    <div id="toDoList">
        <ToDoItem v-for="todo in todos" :name = "todo.name" :type = "todo.type">
            <template #description>
                <p>{{ todo.description }}</p>
            </template>
        </ToDoItem>
    </div>

    <h4 id="numCount">Total Number Of Tasks: {{ todos.length }}</h4>
    
</template>

<script>
import ToDoItem from "./ToDoItem.vue";

export default{
    components: {
        ToDoItem
    },
    data() {
        return {todos: [
        { name: "Do Homework", type: "Not Urgent but Important", description: "Need to do CSC HW" },
        { name: "Leetcode", type: "Urgent", description: "Need to do OA" },
        { name: "Do Personal Project", type: "Not Urgent but Important", description: "Update resume with needed tech stack" }
      ]}
    }
}
</script>