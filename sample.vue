<template>
  <div>
    <p>Name: {{name}}</p>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: ["name"],
};
</script>

<style>
</style>