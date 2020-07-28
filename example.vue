<template>
  <div>
    <h4>Hi there!</h4>
    <hr />
    <my-sample :name="fullName">
      <p>This is a slot content sent from example</p>
    </my-sample>
  </div>
</template>

<script>
import Sample from "./sample";

export default {
  data: function () {
    return {
      fullName: "Ajay Kishore",
    };
  },
  components: {
    "my-sample": Sample,
  },
};
</script>

<style scoped>
</style>