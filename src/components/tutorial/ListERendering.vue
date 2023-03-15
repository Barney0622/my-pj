<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo" />
    <button>Add Todo</button>
  </form>
  <ul>
    <li v-for="todo in todos.value" :key="todo.id">
      {{ todo.text }}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>

<script lang="ts">
import { defineComponent, reactive, ref } from "vue";
import { v4 as uid } from "uuid";

export default defineComponent({
  name: "ListERendering",
  setup() {
    const newTodo = ref("");
    const todos = reactive({
      value: [
        { id: uid(), text: "Java" },
        { id: uid(), text: "springBoot" },
        { id: uid(), text: "TypeScript" },
        { id: uid(), text: "Vue" },
      ],
    });
    const addTodo = () => {
      todos.value.push({
        id: uid(),
        text: newTodo.value,
      });
    };
    const removeTodo = (todo: { id: string }) => {
      // 僅透過過濾顯示剩餘資料，而不是直接刪除數據
      todos.value = todos.value.filter((item) => item.id !== todo.id);
    };
    return {
      todos,
      addTodo,
      newTodo,
      removeTodo,
    };
  },
});
</script>
