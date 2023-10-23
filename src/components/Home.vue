<template>
  <div>Home</div>
  <div> {{ text }}</div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const text = ref('Hola Vue');
    return {
      text,
    }
  }
}
</script>