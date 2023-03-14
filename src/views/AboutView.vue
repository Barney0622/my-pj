<template>
  <div class="about">
    <h1>This is an about page</h1>
    <DeclarativeRendering></DeclarativeRendering>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import DeclarativeRendering from "@/components/tutorial/DeclarativeRendering.vue";

export default defineComponent({
  name: "AboutView",
  components: {
    DeclarativeRendering,
  },
});
</script>
