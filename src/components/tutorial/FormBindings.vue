<template>
  <input v-model="text" placeholder="Type here" />
  <p>{{ text }}</p>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "FormBindings",
  setup() {
    const text = ref("");
    const onInput = (event: InputEvent) => {
      text.value = (event.target as HTMLInputElement).value;
    };

    return {
      onInput,
      text,
    };
  },
});
</script>
