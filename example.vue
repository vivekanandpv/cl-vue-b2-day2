<template>
  <div>
    <h3>{{ counter }}</h3>
    <button @click="clickHandler">Increment</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  methods: {
    clickHandler: function () {
      console.log("increment");
      ++this.counter;
    },
  },
  beforeCreate: function () {
    //  reactivity is not yet in place
    console.log("Before Create", this.counter);
  },
  created: function () {
    //  data, such as counter is reactive now
    console.log("Created", this.counter);
  },
  beforeMount: function () {
    //  template is compiled and v-dom is ready
    //  no data-binding, {{counter}} is plain string now
    //  eq: ngOnInit
    console.log("Before Mount");
  },
  mounted: function () {
    //  data binding completed
    //  native dom is hooked
    //  eq: ngAfterViewInit
    //  use for external data-communication
    console.log("Mounted");
  },
  beforeUpdate: function () {
    //  Vue runtime has recognized the change (state, props) and
    //  ready to call render function (to produce new virtual-node V-Node)
    console.log("Before Update");
  },
  updated: function () {
    //  render function called, new v-node is produced, and updated in V-DOM
    console.log("Updated");
  },
};
</script>

<style scoped>
</style>