<template>
  <div class="flex flex-col justify-center">
    <Todo
      v-for="(todo, index) in $store.state.todos"
      :key="index"
      :todo="todo"
    />
  </div>
</template>

<script>
import { mapState } from "vuex";
import Todo from "./Todo.vue";
export default {
  components: {
    Todo,
  },
  computed: {
    ...mapState({
      todos: "todos",
    }),
  },
};
</script>

<style></style>
