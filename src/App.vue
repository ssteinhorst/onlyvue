<template>
  <div>
    <my-header></my-header>
    <my-search v-bind:providers="providers"></my-search>
    <my-provider v-bind:providers="providers"></my-provider>
  </div>
</template>

<script>

import header from './components/header';
import provider from './components/provider';
import search from './components/search';

import providers from './assets/data.json';

export default {
  name: 'App',
  components: {
    'my-header': header,
    'my-search': search,
    'my-provider': provider
  },
  data: function() {
    return {
      providers: providers.providers,
        baseUrl: process.env.VUE_APP_BASE_URL,

        providers2: [
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
          }
      ]
    };
  },
  methods: {
    created(){
      // Fetch Data
      // this.fetchData();
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 60px;
}
</style>
