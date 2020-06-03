<template>
  <div class="container border">
    <div class="row-no-gutters">
      <div class="col-sm" align="center">Add Provider</div>
    </div>
    <div class="row-no-gutters">
      <div class="col-sm"><input type="text" id="pname" ref="pname"></div>
      <div class="col-sm"><input type="text" id="paddress" ref="paddress"></div>
      <div class="col-sm"><input type="text" id="pphone" ref="pphone"></div>
    </div>
    <button v-on:click="addProvider">Save</button>
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
            })
        }
    },
    props: ['providers']
}
</script>

<style>

</style>