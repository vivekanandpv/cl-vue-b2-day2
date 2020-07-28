<template>
  <div>
    <h4>Hi there!</h4>
    <hr />
    <div v-for="(p, i) in persons" :key="i">
      <my-sample :name="p.fullName" :city="p.city" :country="p.country"></my-sample>
      <hr />
    </div>
  </div>
</template>

<script>
import Sample from "./sample";

export default {
  data: function () {
    return {
      persons: [
        {
          fullName: "Ajay Kumar",
          city: "Bengaluru",
          country: "India",
        },
        {
          fullName: "John Miller",
          city: "London",
          country: "UK",
        },
        {
          fullName: "Roger Godwin",
          city: "Toronto",
          country: "Canada",
        },
      ],
    };
  },
  components: {
    "my-sample": Sample,
  },
};
</script>

<style scoped>
</style>