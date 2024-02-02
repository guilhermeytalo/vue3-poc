<script setup lang="ts">
import {
  Card,
  CardHeader,
  CardTitle,
  CardDescription,
} from '@/components/ui/card'
import {MoreHorizontal, TrendingUp} from 'lucide-vue-next';

defineProps({
  title: String,
  balance: String,
  percents: String,
  month: String,
})
</script>

<template>
  <div class="flex flex-col justify-center items-center">
    <Card class="w-[250px] rounded-3xl">
      <CardHeader>
        <div class="flex justify-between">
          <CardDescription class="font-bold text-inherit">{{ title }}</CardDescription>
          <MoreHorizontal/>
        </div>
        <div class="flex">
          <CardTitle>$ {{ balance }}</CardTitle>
          <span class="ml-2 rounded-full bg-white px-2 py-1 text-xs flex items-center">
            <TrendingUp class="text-green-500 mr-1 w-4"/>
            +{{ percents }}%
          </span>
        </div>
        <CardDescription class="font-bold text-inherit">in {{ month }}</CardDescription>
      </CardHeader>
    </Card>
  </div>
</template>