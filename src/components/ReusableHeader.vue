<!-- eslint-disable vue/multi-word-component-names -->
<template>
  
  <h2 style="margin: 0;">{{ msg }}</h2>
  
</template>

<script setup>
  import { defineProps } from 'vue';

  defineProps({

    msg: {
      type: String,
      required: true,
    }

  });

</script>