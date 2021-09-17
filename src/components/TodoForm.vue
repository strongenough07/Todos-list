<template>
  <div class="mt-10">
    <input
      class="
        focus:ring focus:border-blue-400
        relative
        outline-none
        rounded
        py-1
        px-2
        w-full
        bg-white
        shadow
        text-sm text-gray-700
        placeholder-gray-400
        focus:outline-none focus:shadow-outline
      "
      placeholder="New Todo"
      type="text"
      v-model="newTodoItem"
    />
    <button
      @click="addNewTodoItem()"
      class="
        bg-green-500
        hover:bg-green-700
        text-white
        font-bold
        py-2
        px-4
        rounded-full
        mt-4
      "
    >
      Submit
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: "",
    };
  },
  methods: {
    addNewTodoItem() {
      this.$store.dispatch("addNewTodo", this.newTodoItem);
      this.newTodoItem = "";
    },
  },
};
</script>

<style></style>
