<script setup>
import ThemeSwitch from '../ThemeSwitch.vue';
import IconsComp from '../tools/IconsComp.vue';
</script>

<template>
    <div class="drawer">
        <input id="main-drawer" type="checkbox" class="drawer-toggle" />
        <div class="drawer-content flex flex-col">
            <!-- Navbar with drawer toggle -->
            <div class="w-full navbar bg-base-300">
                <div class="flex-none">
                    <label for="main-drawer" class="btn btn-square btn-ghost drawer-button">
                        <IconsComp name="Menu" />
                    </label>
                    <ThemeSwitch />
                </div>
            </div>
            <!-- Page content -->
            <div class="flex-1">
                <slot name="content"></slot>
            </div>
        </div>
        <div class="drawer-side">
            <label for="main-drawer" class="drawer-overlay"></label>
            <div class="w-200 min-h-full bg-base-200">
                <slot name="sidebar"></slot>
            </div>
        </div>
    </div>
</template>