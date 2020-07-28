<template>
  <div>
    <h4>Hi there!</h4>
    <hr />
    <my-sample :name="fullName">
      <!-- v-slot directive can only be applied to template -->
      <template v-slot:s2>
        <h4>Slot: s2</h4>
      </template>

      <template v-slot:s1>
        <h4>Slot: s1</h4>
      </template>

      <!-- with default slot explicitly defined, will this show? -->
      <!-- <h4>Default slot</h4> -->

      <template v-slot:default>
        <h4>Slot: Default, explicit</h4>
      </template>
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