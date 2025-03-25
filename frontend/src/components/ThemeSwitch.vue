<template>
     <button @click="toggleTheme" class="btn btn-ghost">
      <Icon v-if="theme === 'light'" name="Sun" />
      <Icon v-else name="Moon" />
    </button>
</template>

<script setup>
import { ref, onMounted } from "vue";
import Icon from "./tools/IconsComp.vue";

const theme = ref(localStorage.getItem("theme") || "light");

const toggleTheme = () => {
  theme.value = theme.value === "light" ? "dark" : "light";
  document.documentElement.setAttribute("data-theme", theme.value);
  localStorage.setItem("theme", theme.value);
};

// Beim Laden das gespeicherte Theme setzen
onMounted(() => {
  document.documentElement.setAttribute("data-theme", theme.value);
});
</script>