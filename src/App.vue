<template>
  <Header />
  <TodoList />
</template>

<script>
import "bulma/css/bulma.css";
import Header from "./components/Header.vue";
import TodoList from "@/components/TodoList.vue";

export default {
  name: "App",
  components: {
    Header,
    TodoList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
