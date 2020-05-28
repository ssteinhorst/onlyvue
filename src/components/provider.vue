<template>
    <div class="container">
        <div class="row">
            <div class="col-sm" align="center">
                Providers
            </div>
        </div>
        <div class="row" v-for="provider in providers" :key="provider.name">
            <div class="col-sm">{{ provider.name }}</div>
            <div class="col-sm">{{ provider.address }}</div>
            <div class="col-sm">{{ provider.phone }}</div>
        </div>
      <div class="row">
            <div class="col-sm"><input type="text" id="pname" ref="pname"></div>
            <div class="col-sm"><input type="text" id="paddress" ref="paddress"></div>
            <div class="col-sm"><input type="text" id="pphone" ref="pphone"></div>
      </div>
      <button v-on:click="addProvider">Save</button>
    </div>
</template>

<script>

   export default{
    data: function() {
        return {
            providers: [
                {
                    id: 1,
                    name: 'Steven',
                    address: '12 paper',
                    phone: '555.555.5555'
                },
                                {
                    id: 2,
                    name: 'Jeo',
                    address: '42 towel',
                    phone: '333.555.5555'
                },
                                {
                    id: 1,
                    name: 'Scott',
                    address: 'Lake St',
                    phone: '444.555.5555'
                },
                                {
                    id: 1,
                    name: 'Doctor Strange',
                    address: 'New York',
                    phone: '222.555.5555'
                },
            ]
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
    }
   }

</script>

<style>
    span {
        padding: 3px;
    }
</style>
 