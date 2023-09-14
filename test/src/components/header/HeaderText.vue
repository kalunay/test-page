<script setup>
const props = defineProps({
    title: {
        type: String,
        required: true 
    },
    subtitle: {
        type: String,
        required: true 
    },
    button: {
        type: String,
        default: 'Получить бесплатную консультацию' 
    }
});
</script>

<template>
    <h1>{{ title }}</h1>
    <p>{{ subtitle }}</p>
    <a href="" class="btn">{{ button }}</a>
</template>