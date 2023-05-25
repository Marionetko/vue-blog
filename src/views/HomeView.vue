<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click!</button>
    <button @click="age++">add 1 to age!</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Home',
  setup() {
    // const p = ref(null);

    let name = ref('mario');
    let age = ref(30);

    const handleClick = () => {
      name.value = 'luigi';
      age.value = 35;
    }

    return { name, age, handleClick }
  },
  data() {
    return {
      score: 5
    }
  }
}
</script>
