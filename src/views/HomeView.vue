<script setup>
import { useStorage } from '@/composables/useStorage';

  let food = useStorage('food');

  let age = useStorage('age');

  let obj = useStorage('obj', {one: 'one'})

  setTimeout(() => {
    // obj.value = {'changed': 'entirely'};
    
    obj.value.one = "changed";
  }, 3000) 
</script>

<template>
  <main>
    <p>What is your favourite food? <input type="text" v-model="food" /></p>
    <p>What is your age? <input type="text" v-model="age" /></p>  
  </main>
</template>

