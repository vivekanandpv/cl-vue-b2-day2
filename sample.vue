<template>
  <div>
    <p>Name: {{name}}</p>
    <slot name="s1"></slot>
    <p>------------------</p>
    <slot name="s2"></slot>
    <p>------------------</p>
    <slot></slot>
    <hr />
  </div>
</template>

<script>
export default {
  props: ["name"],
};
</script>

<style>
</style>