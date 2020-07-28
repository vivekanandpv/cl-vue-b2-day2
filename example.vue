<template>
  <div>
    <h4>Hi there!</h4>
    <hr />
    <my-sample :name="fullName" @custom-event="parentHandler"></my-sample>
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
  methods: {
    parentHandler: function (...args) {
      console.log("Example handler called", args);
    },
  },
  components: {
    "my-sample": Sample,
  },
};
</script>

<style scoped>
</style>