<template>
  <div>
    <h2>Calculation of Simple Interest</h2>
    <p>Principal: {{principal}}</p>
    <p>Rate of interest: {{roi}} %</p>
    <p>Term: {{term}} years</p>
    <hr />
    <p>Simple Interest: {{interest}}</p>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      principal: 10000,
      roi: 7.5,
      term: 5,
    };
  },
  computed: {
    interest: function () {
      return (this.principal * this.roi * this.term) / 100;
    },
  },
};
</script>

<style>
</style>