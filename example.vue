<template>
  <div>
    <ul>
      <li v-for="n in 10" :key="n">Current value: {{ n }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      person: {
        name: "Vijay",
        city: "Bengaluru",
        country: "India",
        empCode: 12345,
      },
    };
  },
};
</script>

<style>
</style>