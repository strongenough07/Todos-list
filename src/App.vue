<template>
  <div class="flex flex-col justify-center items-center">
    <img alt="Vue logo" src="./assets/logo.png" />
    <h1 class="text-6xl bold mb-10">Todos</h1>
    <h3 class="text-lg text-center font-bold">
      Completed: {{ completedTodos }}
    </h3>
    <h3 class="text-lg text-center font-bold mb-4">
      Pending: {{ pendingTodos }}
    </h3>
    <TodosList />
    <TodoForm />
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import TodosList from "./components/TodosList.vue";
import TodoForm from "./components/TodoForm.vue";
export default {
  name: "App",
  components: {
    TodosList,
    TodoForm,
  },
  computed: {
    ...mapGetters({
      completedTodos: "completedTodos",
      pendingTodos: "pendingTodos",
    }),
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
