<template>
  <div>
    <div v-for="todo in todos" v-bind:key="todo.id">
      <h3>
        <TodoItem
          v-bind:todo="todo"
          v-on:del-todo="$emit('del-todo', todo.id)"
        />
      </h3>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "Todos",
  components: {
    TodoItem,
  },
  props: { todos: Array },
};
</script>

<style scoped></style>
