<script setup>
import TheWelcome from '@/components/TheWelcome.vue'
import { ref } from 'vue';

let message = ref("hello world");

setTimeout(() => {
  message.value = "I have been Changed";
}, 2000)

</script>

<template>
  <main>
    <TheWelcome />

    <p>{{ message }}</p>

    <p>
      <input type="text" v-model="message" />
    </p>
    
  </main>
</template>
