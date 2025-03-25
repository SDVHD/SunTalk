<script setup>
import { computed } from 'vue';
import Icons from '../../tools/IconsComp.vue';
const props = defineProps({
    item: {
        type: Object,
        required: true
    },
    name: {
        type: String,
        required: true
    },
    ip: {
        type: String,
        required: true
    },
    online: {
        type: Boolean,
        default: false
    }
});
// Compute icon color based on online status
const iconColor = computed(() => props.online ? 'green' : 'red');
</script>

<template>
    <li class="rounded-lg hover:bg-base-300 transition-colors duration-200 ease-in-out cursor-pointer flex p-2">
        <Icons :name="item.icon" size="24" :color="iconColor" />
        <div class="divider divider-horizontal"></div> 
        <div class="flex-1">{{ name }}</div>
        <div class="">{{ ip }}</div>
    </li>
</template>