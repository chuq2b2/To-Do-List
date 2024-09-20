<template>
  <div id="heading">
    <h1> To Do List</h1>
  </div>
  <ToDoList/>

</template>

<script>
import ToDoList from './components/ToDoList.vue'

export default {
    components: {
        ToDoList
    }
}
</script>