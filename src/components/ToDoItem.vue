<template>
    <div class="toDoItem">
      <h2 class="toDoName">{{ name }}</h2> <!-- Display name as <h2> -->
      <h4>{{ type }}</h4> <!-- Display type as <h4> -->
      <slot name="description"></slot> <!-- Keep description as a slot -->
        <div id = "statusUpdate">
            <button @click="$emit('completedToDo', name)">
                Completed
            </button>
        </div>
    </div>
  </template>

<script>
export default {
  props: ['name', 'type', 'desc'],
  emits: ['completedToDo']
};
</script>