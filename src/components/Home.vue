<template>
  <div>Home</div>
  <div> {{ fullName }}</div>
</template>

<script>

import { toRefs, computed } from "vue";

export default {
  props: {
    firstName: String, 
    lastName: String,
  },
  setup(props) {
    const { firstName, lastName } = toRefs(props);
    const fullName = computed(() => {
      return `${firstName.value} ${lastName.value}`
    })
    return {
      fullName
    }
  }
}
</script>