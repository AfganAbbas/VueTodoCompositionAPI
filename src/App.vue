<template>
  <div>
    <h1>HelloWorld</h1>
    <InputTab @addtolist="addToList" />
    <ToDoList :todos="todos" />
  </div>
</template>

<script>
import ToDoList from "./components/ToDoList.vue";
import InputTab from "./components/InputTab.vue";
import { ref } from "vue";

export default {
  name: "App",
  components: {
    ToDoList,
    InputTab,
  },
  setup() {
    const todos = ref([]);
    const addToList = (inp) => {
      todos.value.push(inp.value);
      console.log(todos.value);
    };
    return { todos, addToList };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
