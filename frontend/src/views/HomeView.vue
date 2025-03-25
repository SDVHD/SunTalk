<script setup>
import MainView from '@/components/MainView.vue';
import ChannelCard from '@/components/channels/ChannelCard.vue';
import ChannelLayout from '@/components/channels/ChannelLayout.vue';
import IconsComp from '@/components/tools/IconsComp.vue';
</script>

<template>
    <MainView maincontent-title="Channels" sidemenu="true" sidemenuTitle="SunTalk">
        <!-- Main Content -->
        <ChannelLayout>
            <ChannelCard channelName="Production" memberCount="10" />
            <ChannelCard channelName="Video" memberCount="5" />
            <ChannelCard channelName="Audio" memberCount="3" />
            <ChannelCard channelName="Light" memberCount="2" />
            <ChannelCard channelName="Visuals" memberCount="1" />
            <ChannelCard channelName="Troubleshooter" memberCount="0" />
        </ChannelLayout>
    </MainView>
</template>