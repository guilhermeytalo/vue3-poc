<template>
  <div>
    <!-- Card Container-->
    <div class="flex ml-16">
      <CardComponent
          v-for="(card, index) in cards"
          :key="index"
          :title="card.title"
          :balance="card.balance"
          :percents="card.percents"
          :month="card.month"
      />
    </div>
  </div>
</template>
<script setup lang="ts">
import {reactive} from 'vue';
import CardComponent from "~/components/CardComponent.vue";

const cards = reactive([
  {title: "Total Balance", balance: "47, 651", percents: "12.5", month: "October"},
  {title: "Sales", balance: "23,124", percents: "24.8", month: "October"},
]);
</script>