<template>
  <div class="container border">Search
    <div class="row">
      <div class="col-sm" align="center">
        <input type="text" id="pname" ref="pname" placeholder="Name search">
      </div>
      <div class="col-sm" align="center">
        <input type="text" id="paddress" ref="paddress" placeholder="Zone search">
      </div>
      <div class="col-sm" align="center">
        <input type="text" id="pphone" ref="pphone" placeholder="Therapy search">
      </div>
    </div>
    <div class="row">
      <button v-on:click="addProvider">Go</button>
    </div>
  </div>
</template>

<script>
  export default {
    data: function() {
      return {

      };
    },
    methods: {
      addProvider: function() {
        this.providers.push({
          name: this.$refs.pname.value,
          address: this.$refs.paddress.value,
          phone: this.$refs.pphone.value
        });
      }
    },
    props: ['providers']
  }
</script>

<style>

</style>