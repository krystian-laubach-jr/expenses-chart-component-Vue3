<template>
  <div id="content">

    <ExpensesChartComponent/>
    
  </div>
</template>

<script setup>

  import ExpensesChartComponent from './components/ExpensesChartComponent.vue';

</script>

<style>

  body {
    margin: 0;
    padding: 0;
  }

  #content{
    width: 100vw;
    height: 100vh;

    background-color: hsl(27, 66%, 92%);

    display: flex;
    align-items: center;
    justify-content: center;
  }

</style>