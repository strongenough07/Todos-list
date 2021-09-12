<template>
  <div class="flex flex-col justify-center items-center">
    <img alt="Vue logo" src="./assets/logo.png" />
    <h1 class="text-6xl bold mb-10">Todos</h1>
    <TodosList />
    <TodoForm />
  </div>
</template>

<script>
import TodosList from "./components/TodosList.vue";
import TodoForm from "./components/TodoForm.vue";
export default {
  name: "App",
  components: {
    TodosList,
    TodoForm,
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
