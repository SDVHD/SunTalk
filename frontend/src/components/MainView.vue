<script setup>
import MainLayout from './layout/MainLayout.vue';
import SideMenu from './layout/SideMenu.vue';
import MainContent from './layout/MainContent.vue';
import ThemeSwitch from './ThemeSwitch.vue';

const props = defineProps({
    sidemenu: Boolean,
    sidemenuTitle: String,
    maincontentTitle: String,
});

</script>

<template>
    <MainLayout>
        <template v-if="sidemenu">
            <SideMenu :title="sidemenuTitle">
               
            </SideMenu>
        </template>
        <MainContent :title="maincontentTitle">
            <slot></slot>
        </MainContent>
        <ThemeSwitch />
    </MainLayout>
</template>