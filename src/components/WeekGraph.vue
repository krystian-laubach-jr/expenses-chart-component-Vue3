<template>
  
<div id="graph">

  <GraphBar v-for="(data, index) in calculatedWeekData" :key="index" :barData="data" />

</div>
  
</template>

<script setup>
  import { ref } from 'vue';
  import GraphBar from './GraphBar.vue';
  import { data } from '@/data/data'

 let rawData = ref(data);

  const getBiggestExpenses = (rawData) => {
    return Math.max(...rawData.value.map(day => day.amount));
  }

  const calculateWeekData = (rawData) => {
    let biggestExpenses = getBiggestExpenses(rawData);

    return rawData.value.map(day => ({
      ...day,
      pillarType: (day.amount === biggestExpenses) ? "largest pillar" : "pillar",
      height: `${(day.amount / biggestExpenses) * 60}%`
    }));

  };

  const calculatedWeekData = calculateWeekData(rawData)
</script>

<style>

  #graph {
    height: 47.5% ;

    display: flex;
    justify-content: space-between;

    margin-bottom: 2.5%;
  }

</style>