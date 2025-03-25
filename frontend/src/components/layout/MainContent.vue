<script setup>
import { watch, ref } from 'vue';

const props = defineProps({
    title: String,
});
</script>

<template>
    <main class="flex-1 p-6 bg-base-100">
        <h2 class="text-2xl font-bold mb-4">{{ title }}</h2>
        <div class="divider"></div>
        <slot></slot>
    </main>
</template>