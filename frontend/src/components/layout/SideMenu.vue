<script setup>
import IconsComp from '../tools/IconsComp.vue';
import { RouterLink } from 'vue-router';
const props = defineProps({
    title: String,
});
</script>

<template>
    <div class="p-4">
        <h1 class="text-xl font-bold mb-1">{{ title }}</h1>
        <div class="divider mb-4"></div>
        <div class="menu p-4 w-full">
            <ul>
                <!-- Menu Header -->
                <li class="menu-title">
                    <span>Navigation</span>
                </li>
                <!-- Menu Items -->
                <li>
                    <RouterLink to="/">
                        <IconsComp name="Home" />
                        Dashboard
                    </RouterLink>
                </li>
                <li>
                    <RouterLink to="/users">
                        <IconsComp name="Users" />
                        Users
                    </RouterLink>
                </li>
                <li>
                    <RouterLink to="/settings">
                        <IconsComp name="Settings" />
                        Settings
                    </RouterLink>
                </li>
            </ul>
        </div>
    </div>
</template>