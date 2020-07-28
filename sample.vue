<template>
  <div>
    <p>Name: {{name}}</p>
    <slot>If you do not pass slot content, default would appear!</slot>
  </div>
</template>

<script>
export default {
  props: ["name"],
};
</script>

<style>
</style>