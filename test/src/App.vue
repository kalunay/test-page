<script setup>
import HeaderView from './components/HeaderView.vue';
import FooterView from './components/FooterView.vue';
import MapView from './components/MapView.vue';
import NewsList from './components/NewsList.vue';
import ServicesView from './components/ServicesView.vue';
import TableView from './components/TableView.vue'
import PriceView from './components/PriceView.vue';
import FeaturesView from './components/FeaturesView.vue';
import FeedbackView from './components/FeedbackView.vue';
import ModalVuew from './components/UI/ModalVuew.vue';
</script>

<template>
  <HeaderView />
  <main>
    <FeaturesView />
    <PriceView />
    <TableView />
    <ServicesView />
    <NewsList />
    <FeedbackView />
    <MapView />
  </main>
  <FooterView />
  <ModalVuew />
</template>

<style scoped>

</style>
