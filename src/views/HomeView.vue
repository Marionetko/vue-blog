<template>
  <div class="home">
    home
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click!</button>
  </div>
</template>

<script>


export default {
  name: 'Home',
  setup() {
    console.log('setup');

    let name = 'mario';
    let age = 30;

    const handleClick = () => {
      console.log("clicked")
    }

    return { name, age, handleClick }
  }
}
</script>
