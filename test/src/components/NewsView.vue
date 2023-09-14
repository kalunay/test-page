<script setup>
import ImageView from './UI/ImageView.vue';

const props = defineProps({
    item: {
        type: Object,
        required: true
    }
}) 
</script>

<template>
    <div class="news__list-item">
        <div class="image">
            <ImageView :src="item.image" :alt="item.name" />
        </div>
        <div class="content">
            {{ item.name }}
            <span>{{ item.date }}</span>
        </div>
    </div>
</template>