<template>

  <div id="container">

    <Balance/>

    <SpendingContainer/>

  </div>

</template>

<script setup>

  import Balance from './Balance.vue';
  import SpendingContainer from './SpendingContainer.vue';

</script>

<style>

  #container {
    width: 90%;
    height: 80%;

    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  #container > *{
    border-radius: 25px;
  }

  @media (min-width: 1024px) {
    #container {
      width: 40%;
      height: 75%;
        
    }
  }
</style>