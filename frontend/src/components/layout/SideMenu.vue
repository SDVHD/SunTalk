<script setup>
const props = defineProps({
    title: String,
});
</script>

<template>
    <div class="p-4">
        <h1 class="text-xl font-bold mb-1">{{ title }}</h1>
        <div class="divider mb-4"></div>
        <slot></slot>
    </div>
</template>