<script setup>
import MainView from '@/components/MainView.vue';
import ChannelCard from '@/components/channels/ChannelCard.vue';
import ChannelLayout from '@/components/channels/ChannelLayout.vue';
</script>

<template>
    <MainView maincontent-title="Channels">
        <ChannelLayout gridColumns="5">
            <ChannelCard channelName="Production" memberCount="10" />
            <ChannelCard channelName="Video" memberCount="5" />
            <ChannelCard channelName="Audio" memberCount="3" />
            <ChannelCard channelName="Light" memberCount="2" />
            <ChannelCard channelName="Visuals" memberCount="1" />
            <ChannelCard channelName="Troubleshooter" memberCount="0" />
        </ChannelLayout>
    </MainView>
</template>