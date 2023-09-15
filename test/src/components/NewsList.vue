<script setup>
import NewsView from './NewsView.vue';
import { news } from "../constants";
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import { ref } from 'vue';

const breakpoints = ref({
    320: {
        itemsToShow: 1,
        snapAlign: 'center',
    },
    480: {
        itemsToShow: 1,
        snapAlign: 'center',
    },
    768: {
        itemsToShow: 2,
        snapAlign: 'start',
    },
    1024: {
        itemsToShow: 3,
        snapAlign: 'start',
    },
});

</script>

<template>
    <div class="news">
        <div class="container">
        <div class="news__header">Новости</div>
        <div class="news__list">
            <!-- <NewsView v-for="item in news" :item="item" :key="item.id" /> -->
            <carousel :itemsToShow="3" :breakpoints="breakpoints">
                <slide v-for="item in news" :key="item.id">
                    <NewsView :item="item" />
                </slide>

                <template #addons>
                <navigation />
                <pagination />
                </template>
            </carousel>
        </div>
        </div>
    </div>

</template>