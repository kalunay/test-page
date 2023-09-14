<script setup>
import NewsView from './NewsView.vue';
import { news } from "../constants";
</script>

<template>
    <div class="news">
        <div class="container">
        <div class="news__header">Новости</div>
        <div class="news__list">
            <NewsView v-for="item in news" :item="item" :key="item.id" />
        </div>
        </div>
    </div>
</template>