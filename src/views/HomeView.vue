<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Click!</button>
    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }} - {{ nameTwo }}</p>
    <button @click="updateNinjaTwo">Update ninja two</button>
  </div>
</template>

<script>
import { ref, reactive } from 'vue';

export default {
  name: 'Home',
  setup() {
    const ninjaOne = ref({ name: 'mario', age: 30 });
    const ninjaTwo = reactive({ name: 'luigi', age: 35});

    const nameOne = ref('mario');
    const nameTwo = reactive('luigi'); //not reactive (can't use primitive value)

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40;
    }

    const updateNinjaTwo = () => {
      ninjaTwo.age = 45;
      nameTwo = 'mario'; // not working
    }

    return { ninjaOne, ninjaTwo, updateNinjaOne, updateNinjaTwo, nameTwo }
  }
}
</script>
