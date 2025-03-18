<template>
  <div id="content">

    <temp/>
    
  </div>
</template>

<script setup>

  import temp from './components/temp.vue';

</script>

<style>

  body {
    margin: 0;
    padding: 0;
  }

  #content{
    width: 100vw;
    height: 100vh;

    display: flex;
    align-items: center;
    justify-content: center;
  }

</style>