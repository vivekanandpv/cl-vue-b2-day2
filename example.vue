<template>
  <div>
    <label for="basePrice">Base Price</label>
    <input type="text" id="basePrice" v-model="basePrice" />
    <hr />
    <h4>Final Price: {{finalPrice}}</h4>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      basePrice: 1,
      taxRate: 7.5,
    };
  },
  computed: {
    finalPrice: function () {
      return +this.basePrice + (this.basePrice * this.taxRate) / 100;
    },
  },
  watch: {
    basePrice: function (newValue, oldValue) {
      console.log(`Base price changed from ${oldValue} to ${newValue}`);
    },
  },
};
</script>

<style>
</style>