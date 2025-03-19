<template>
  
<div id="graph">

  <GraphBar v-for="(data, index) in calculatedWeekData" :key="index" :barData="data" />

</div>
  
</template>

<script setup>

  import GraphBar from './GraphBar.vue';

  const rawData = [
    { weekDay: 'mon', amount: 594 },
    { weekDay: 'tue', amount: 556 },
    { weekDay: 'wed', amount: 998 },
    { weekDay: 'thu', amount: 768 },
    { weekDay: 'fri', amount: 598 },
    { weekDay: 'sat', amount: 492 },
    { weekDay: 'sun', amount: 617 }
  ];

  const getBiggestExpenses = (rawData) => {
    return Math.max(...rawData.map(day => day.amount));
  }

  const calculateWeekData = (rawData) => {
    let biggestExpenses = getBiggestExpenses(rawData);

    return rawData.map(day => ({
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