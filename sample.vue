<template>
  <div>
    <p>Name: {{name}}</p>
    <p>City: {{city}}</p>
    <p>Country: {{country}}</p>
  </div>
</template>

<script>
export default {
  props: ["name", "city", "country"],
};
</script>

<style>
</style>