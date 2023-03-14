<template>
  <h1 :class="titleClass">Make me red</h1>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "AttributeBindings",
  setup() {
    const titleClass = ref("title");
    return {
      titleClass,
    };
  },
});
</script>

<style>
.title {
  color: red;
}
</style>
