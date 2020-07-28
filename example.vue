<template>
  <div>
    <button @click="clickHandler('Hi there!', 100, {year: 2005})">Click me!</button>
  </div>
</template>

<script>
export default {
  methods: {
    clickHandler: function (...args) {
      console.log(args);
    },
  },
};
</script>

<style>
</style>