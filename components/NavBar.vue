<template>
  <div class="fixed top-0 right-0">
    <button class="btn btn-square btn-ghost" @click="toggleMenu">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="currentColor"
        className="size-6">
        <path strokeLinecap="round" strokeLinejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5M12 17.25h8.25" />
      </svg>
    </button>
    <Menu v-if="isMenuOpen" @close="isMenuOpen = false" />
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import Menu from './Menu.vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style>

</style>