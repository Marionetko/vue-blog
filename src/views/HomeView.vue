<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click!</button>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Home',
  setup() {
    console.log(this)

    const p = ref('hello');
    console.log(p, p.value)

    let name = 'mario';
    let age = 30;

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add('test');
      p.value.textContent = 'yo-yo-yo';
    }

    return { name, age, handleClick, p }
  }
}
</script>
