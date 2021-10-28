<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <TodoList></TodoList>
  </div>
</template>

<script>
import TodoHeader from "./components/TodoHeader";
import TodoInput from "./components/TodoInput";
import TodoList from "./components/TodoList";

export default {
  name: "App",
  components: {
    TodoHeader,
    TodoInput,
    TodoList,
  },
};
</script>

<style lang="scss">
@import "./assets/reset.css";
@import "./assets/common.scss";
</style>