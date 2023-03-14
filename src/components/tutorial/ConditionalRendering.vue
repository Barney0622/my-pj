<template>
  <button @click="toggle">toggle</button>
  <h1 v-if="awesome.value">This is awesome!</h1>
  <h1 v-else>Not awesome!</h1>
</template>

<script lang="ts">
import { defineComponent, reactive } from "vue";

export default defineComponent({
  name: "ConditionalRendering",
  setup() {
    const awesome = reactive({
      value: false,
    });
    const toggle = () => {
      awesome.value = !awesome.value;
    };
    return {
      toggle,
      awesome,
    };
  },
});
</script>
