<template>
  <div>
    <div v-for="(value, name, index) in person" :key="index">
      <p>{{index}}. {{name}} -> {{value}}</p>
    </div>
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