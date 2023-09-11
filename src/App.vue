<script setup>
  import { ref } from 'vue';
  import Menu from './components/Menu.vue';
  const show = ref(true);
</script>

<template>
  <button @click="show = !show">Menú</button>
  <transition name="fade">
    <Menu v-show="show"/>
  </transition>
</template>

<style scoped>

.fade-enter-from {
  opacity: 0;
}
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active, .fade-enter-active {
  transition: opacity 0.5s ease;
}

</style>
