<template>
  <div>
    <!-- <NuxtWelcome /> -->
    <CardComponent title="Total Balance" balance="47, 651" percents="12.5" month="October"/>
    <CardComponent title="Sales" balance="23,124" percents="24.8" month="October"/>
  </div>
</template>
<script setup lang="ts">
import CardComponent from "~/components/CardComponent.vue";
</script>