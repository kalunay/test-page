<script setup>
import { features, featuresTitle } from "../constants";
import FeatureItemView from "./FeatureItemView.vue";
</script>

<template>
    <div class="features">
      <div class="container">
        <div class="features__header">{{ featuresTitle }}</div>
        <div class="features__lists">
          <FeatureItemView v-for="feature in features" :feature="feature" :key="feature.id" />
        </div>
      </div>
    </div>
</template>