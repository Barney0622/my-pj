<template>
  <h1>{{ message }}</h1>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "DeclarativeRendering",
  setup() {
    const message = ref("HelloWorld!");

    return {
      message,
    };
  },
});
</script>
