<template>
  <div>
    <h4>Hi there!</h4>
    <hr />
    <my-sample></my-sample>
  </div>
</template>

<script>
import Sample from "./sample";

export default {
  components: {
    "my-sample": Sample,
  },
};
</script>

<style scoped>
</style>