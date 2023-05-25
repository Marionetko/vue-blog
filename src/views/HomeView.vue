<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Click!</button>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Home',
  setup() {
    const ninjaOne = ref({ name: 'mario', age: 30 });

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40;
    }

    return { ninjaOne, updateNinjaOne }
  },
  data() {
    return {
      score: 5
    }
  }
}
</script>
