<template>
  
  <div id="expenses">
    <ReusableHeader/>
    <WeekGraph/>
    <MonthlyTotal/>
  </div>
  
</template>

<script setup>

  import ReusableHeader from './ReusableHeader.vue';
  import WeekGraph from './WeekGraph.vue';
  import MonthlyTotal from './MonthlyTotal.vue';

</script>

<style>

  #expenses {
    width: 100%;
    height: 75%;

    background-color: hsl(33, 100%, 98%);

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;

  }

  #expenses > * {
    width: 90%;
  }

</style>