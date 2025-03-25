<script setup>

const props = defineProps({
    title: String,
});
</script>

<template>
    <!-- Seitenmenü -->
    <aside class="w-80 bg-base-200 p-5 flex flex-col">
        <h1 class="text-xl font-bold mb-1">{{ title }}</h1>
        <div class="divider mb-4"></div>
        <slot></slot>
    </aside>
</template>
