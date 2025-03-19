<template>
  
<div id="graph">

  <GraphBar v-for="(data, index) in weekData" :key="index" :barData="data" />

</div>
  
</template>

<script setup>

  import GraphBar from './GraphBar.vue';

  const weekData = [
    { weekDay: 'mon', pillarType: 'pillar',         height: '24%', amount: 594 },
    { weekDay: 'tue', pillarType: 'pillar',         height: '52%', amount: 556 },
    { weekDay: 'wed', pillarType: 'pillar',         height: '38%', amount: 698 },
    { weekDay: 'thu', pillarType: 'largest pillar', height: '28%', amount: 764 },
    { weekDay: 'fri', pillarType: 'pillar',         height: '62%', amount: 598 },
    { weekDay: 'sat', pillarType: 'pillar',         height: '10%', amount: 392 },
    { weekDay: 'sun', pillarType: 'pillar',         height: '23%', amount: 617 }
  ];

</script>

<style>

  #graph {
    height: 47.5% ;

    display: flex;
    justify-content: space-between;

    margin-bottom: 2.5%;
  }

</style>