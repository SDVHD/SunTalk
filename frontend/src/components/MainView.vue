<script setup>
import MainLayout from './layout/MainLayout.vue';
import SideMenu from './layout/SideMenu.vue';
import MainContent from './layout/MainContent.vue';
import IconsComp from './tools/IconsComp.vue';

const props = defineProps({
    sidemenu: Boolean,
    sidemenuTitle: String,
    maincontentTitle: String,
});
</script>

<template>
    <MainLayout>
        <template #sidebar v-if="sidemenu">
            <SideMenu :title="sidemenuTitle">
                <slot name="sidebar"></slot>
            </SideMenu>
        </template>
        <template #content>
            <div class="navbar lg:hidden">
                <div class="flex-none">
                    <label for="main-drawer" class="btn btn-square btn-ghost drawer-button">
                        <IconsComp name="Menu" />
                    </label>
                </div>
            </div>
            <MainContent :title="maincontentTitle">
                <slot></slot>
            </MainContent>
        </template>
    </MainLayout>
</template>