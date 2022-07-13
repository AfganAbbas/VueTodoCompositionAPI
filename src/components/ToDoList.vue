<template>
  <div>
    <h1>To Do List</h1>
    <div class="to-do-list">
      <v-card class="mx-auto" max-width="400" tile>
        <ToDo v-for="todo in todos" :todo="todo" :key="todos.indexOf(todo)"
      /></v-card>
    </div>
  </div>
</template>

<script>
import ToDo from "./ToDo.vue";

export default {
  components: {
    ToDo,
  },
  props: ["todos"],
  setup(props) {},
};
</script>

<style></style>
