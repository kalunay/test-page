<script setup>
const props = defineProps({
    links: {
        type: Array,
        required: true
    },
    class: {
        type: String
    }
})
</script>

<template>
    <ul :class="class">
        <li v-for="link in links" :key="link.id">
            <a :href="link.link">{{ link.name }}</a>
        </li>
    </ul>
</template>