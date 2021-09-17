<template>
  <div
    class="
      flex flex-row
      items-center
      focus:ring focus:border-blue-400
      rounded
      py-1
      px-2
      w-full
      bg-white
      shadow
      text-sm text-gray-700
      placeholder-gray-400
      focus:outline-none focus:shadow-outline
      mb-2
    "
  >
    <span
      :class="{ completed: todo.completed }"
      @click="toggleTodoStatus(todo)"
    >
      {{ todo.title }}
    </span>
    <button
      @click="deleteTodo(todo)"
      class="
        hover:text-red-500
        text-red-400
        font-bold
        p-2
        rounded
        inline-flex
        items-center
      "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="w-6 h-6"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"
        />
      </svg>
    </button>
  </div>
</template>

<script>
import { mapActions } from "vuex";

export default {
  props: ["todo"],
  methods: {
    ...mapActions({
      deleteTodo: "deleteTodo",
      toggleTodoStatus: "toggleTodoStatus",
    }),
  },
};
</script>

<style scoped>
.completed {
  text-decoration: line-through;
}
</style>
>
