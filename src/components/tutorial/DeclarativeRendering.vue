<template>
  <h1>{{ message }}</h1>
  <h1>count: {{ counter.count }}</h1>
</template>

<script lang="ts">
import { defineComponent, ref, reactive } from "vue";

export default defineComponent({
  name: "DeclarativeRendering",
  setup() {
    const message = ref("HelloWorld!");
    const counter = reactive({
      count: 0,
    });
    return {
      message,
      counter,
    };
  },
});
</script>
