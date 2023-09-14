<script setup>
import { preiceList, priceTitle, subPriceTitle } from "../constants";
</script>

<template>
    <div class="price">
      <div class="container">
        <div class="price__header">{{ priceTitle }}</div>
      </div>
      <div class="price__list">
        <div class="price__list-header">{{ subPriceTitle }}</div>
        <ul>
          <li v-for="item in preiceList">{{ item.name }}</li>
        </ul>
      </div>
    </div>
</template>