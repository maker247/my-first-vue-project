<!-- <script>

export default {
  methods: {
    flash(message) {
      alert(message)
    }
  }
}

</script>

<template>
  <main>
    <TheWelcome />
    <button @click="flash('hello')">click me</button>
  </main>
</template> -->

<script setup>
  import { useFlash } from '@/composables/useFlash';

  let {flash} = useFlash();
</script>

<template>
  <main>
    <TheWelcome />
    <button @click="flash('hello')">click me</button>
  </main>
</template>

