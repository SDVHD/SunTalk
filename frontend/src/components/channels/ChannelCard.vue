<script setup>
import IconsComp from '../tools/IconsComp.vue';

defineProps({
    channelName: {
        type: String,
        required: true,
    },
    memberCount: {
        type: Number,
        default: 0,
    }
})
</script>

<template>
    <div class="card w-96 bg-base-100 shadow-xl hover:shadow-2xl transition-shadow">
        <div class="card-body">
            <div class="flex items-center justify-between">
                <div class="flex items-center gap-3">
                    <i class="fas fa-volume-up text-primary"></i>
                    <div>
                        <h2 class="card-title">{{ channelName }}</h2>
                        <p class="text-sm text-base-content/70">
                            {{ memberCount }} members online
                        </p>
                    </div>
                </div>
                <div class="card-actions">
                    <button class="btn btn-primary btn-circle">
                        <IconsComp name="Headphones" />
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>