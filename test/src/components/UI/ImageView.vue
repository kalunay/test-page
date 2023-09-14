<script setup>
import { pathImg } from "../../constants";
const props = defineProps({
    src: {
        type: String,
        required: true
    },
    alt: {
        type: String,
        default: ''
    }
})
</script>

<template>
    <img :src="`${pathImg}${src}`" :alt="alt">
</template>