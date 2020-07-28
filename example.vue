<template>
  <div>
    <!-- Fired only once -->
    <button @click.once="clickHandler('once')">Click (once)</button>
    <hr />
    <!-- No page reload; useful for form submission -->
    <button @click.prevent="clickHandler('prevent')">Click (prevent)</button>
    <hr />
    <!-- Child events are not considered -->
    <div @click.self="clickHandler('self')" class="card">
      <button>Click (self-at-outer)</button>
    </div>
    <hr />
    <!-- Child events are prioritized for parent -->
    <div @click.capture="clickHandler('capture outer')" class="card">
      <button @click="clickHandler('capture inner')">Click (capture-out-then-in)</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    clickHandler: function (args) {
      console.log("Clicked", args);
    },
  },
};
</script>

<style>
</style>