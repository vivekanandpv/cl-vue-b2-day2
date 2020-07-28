<template>
  <div>
    <label for="basePrice">Base Price</label>
    <input type="text" id="basePrice" v-model="basePrice" />
    <hr />
    <label for="finalPrice">Final Price</label>
    <input type="text" id="finalPrice" v-model="finalPrice" />
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      basePrice: 10000,
      taxRate: 7.5,
    };
  },
  computed: {
    finalPrice: {
      get: function () {
        return this.basePrice + (this.basePrice * this.taxRate) / 100;
      },
      set: function (newFinalPrice) {
        this.basePrice = (newFinalPrice * 100) / (100 + this.taxRate);
      },
    },
  },
};
</script>

<style>
</style>