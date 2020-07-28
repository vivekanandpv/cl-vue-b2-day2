<template>
  <div>
    <ul v-for="n in 10" :key="n">
      <li>Current value: {{n}}</li>
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