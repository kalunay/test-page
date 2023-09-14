<script setup>
import ImageView from './UI/ImageView.vue';
const props = defineProps({
    feature: {
        type: Object,
        required: true
    }
});
</script>
<template>
    <div class="features__lists-item">
        <div class="features__lists-item-icon">
        <ImageView :src="feature.image" />
        </div>
        <span>{{ feature.name }}</span>
        {{ feature.text }}
    </div>
</template>