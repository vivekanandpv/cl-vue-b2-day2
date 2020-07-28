<template>
  <div>
    <button @click="clickHandler">Click me to emit custom event</button>
  </div>
</template>

<script>
export default {
  props: ["name"],
  methods: {
    clickHandler: function () {
      this.$emit("custom-event", 100, "Hi there!", { name: "Mohan" });
    },
  },
};
</script>

<style>
</style>